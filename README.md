# App47 PhoneGap plugin iOS Example Project

Clone this repository (or download the tar ball) and then proceed to import the sample project (in the 2.x directory, for example) using XCode. Note, the plugin in use in this project can be found at the [App47 PhoneGap plugins repository](https://github.com/App47/phonegap-plugins).

## Getting started with PhoneGap iOS and App47's Android Agent

1. Download the [App47 iOS Agent](http://app47.com/wiki/doku.php?id=configure:iosapp) from the [App47 Dashboard](https://cirrus.app47.com)
2. Follow the directions for integrating the iOS Agent into an XCode app -- be sure to add the corresponding folder in your project you copied the various binary assets into. 
3. Be sure to add your App's ID (which can be found in the App47 Dashbard) into the `EmbeddedAgentSettings.plist` file. 
4. In the PhoneGap `AppDelegate.m` file (found in the `Classes` directory), add:
```
#import "EmbeddedAgent.h"
``` 
and in the `didFinishLaunchingWithOptions` method add:
```
[EmbeddedAgent configureAgent]; 
```
5. Grab the [iOS App47 PhoneGap plugin](https://github.com/App47/phonegap-plugins) and place the `app47pg.js` file in the `www/js` directory.
6. Copy the plugin files `App47PGPlugin.h` and `App47PGPlugin.m` into the `Plugins` directory within the `Classes` directory of your project.
7. Be sure to update the PhoneGap `config.xml` file to include the newly installed App47 plugin:
```
<plugin name="App47" value="App47PGPlugin" />
```


# License

The MIT License

Copyright (c) 2011 App47, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE