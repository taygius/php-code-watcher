php-code-watcher
===========

Auto running phpcodesniffer for you project when files was changed. Run php codesniffer for changed file only
Works on ubuntu over 

tests for nodejs/coffee project in Ubuntu
   and notificating to notify-osd

## Dependences

1)
Working on ubuntu over 11.04
Unity

2)
Setup 'inotify-tools' for watching file changes
``` bash
sudo apt-get install inotify-tools
sudo apt-get install php-codesniffer
```

3)
Setup patched notify-osd *optional
``` bash
sudo add-apt-repository ppa:leolik/leolik 
sudo apt-get update && sudo apt-get upgrade 
sudo apt-get install libnotify-bin 
echo 'bubble-expire-timeout = 1sec' >> ~/.notify-osd
```

## How to run

* change PHPCS_STANDARD with needed
* run 
``` bash
sh ./codewatcher /path/to/project
```

## Options

Also you can edit follow options in 'codewatcher.sh':

PHPCS_STANDARD      - name or path to codesniffer's standart 
TMP_FILE            - path to temp file
NOTIFY_ICON_SUCCESS - path to success icon - 128x128 recommended
NOTIFY_ICON_ERROR   - path to error icon - 128x128 recommended
NOTIFY_TIME         - time of showing notify message, ms

## License

The MIT License

Copyright (c) 2012 taygius

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.