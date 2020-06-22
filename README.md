# IME

This application demonstrates usage of Tizen IME - the on-screen keyboard.

The idea is very simple - if user navigates to `input` or `textarea` field and focuses it
the default behaviour of Tizen platform is to display the system built-in on-screen keyboard
and application can get the text input from user.


## How to use the application

Use TV remote controller to navigate to text input field and press **ENTER**. IME will appear.
Type whatever you want and choose **DONE**.

The code of the application demonstrates how to handle IME and how to get the user input.
In general it consists of event handlers for focusing `input` element
and key handlers for **Done** and **Cancel** buttons of IME. Those buttons trigger key events
that can be handled in the application (no need to register those keys -
they are already registered by platform implicitly just like **arrows** and **ENTER** buttons).


## Supported platforms

2015 and newer


### Prerequisites

Please notice that it is important to focus the `document.body` on application start.


### Privileges and metadata

No privileges nor metadata are needed to use IME itself.
In order to use the TV remote controller only the following privilege has to be included in `config.xml`:

```xml
<tizen:privilege name="http://tizen.org/privilege/tv.inputdevice" />
```

### File structure

```
IME/ - IME sample app root folder
│
├── assets/ - resources used by this app
│   │
│   └── JosefinSans-Light.ttf - font used in application
│
├── css/ - styles used in the application
│   │
│   ├── main.css - styles specific for the application
│   └── style.css - style for application's template
│
├── js/ - scripts used in the application
│   │
│   ├── init.js - script that runs before any other for setup purpose
│   ├── keyhandler.js - module responsible for handling keydown events
│   ├── logger.js - module allowing user to register logger instances
│   ├── main.js - main application script
│   ├── navigation.js - module responsible for handling in-app focus and navigation
│   └── utils.js - module with useful tools used through application
│
├── CHANGELOG.md - changes for each version of application
├── config.xml - application's configuration file
├── icon.png - application's icon
├── index.html - main document
└── README.md - this file
```

## Other resources

*  **Keyboard/IME on developer.samsung.com**  
  https://developer.samsung.com/tv/develop/guides/user-interaction/keyboardime



## Copyright and License

**Copyright 2019 Samsung Electronics, Inc.**

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
