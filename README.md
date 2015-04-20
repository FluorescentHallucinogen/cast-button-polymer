Copyright 2014 Google Inc. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

#cast-button-polymer
This element renders the cast button and manages it's states.  This button uses polymer for data binding and rendering, to find out more about Polymer take a look at the [Polymer documentation](https://www.polymer-project.org).

#Overview
This button starts by detecting if a cast device is available, it's hidden by default and becomes visible if a device is found.  It also displays a tool tip to notify of the button onclick action.

Clicking the button to start the cast selection process also starts the connection animation.

Once a cast connection is established the button is overlayed in blue.

When connected, you can use the CastManager methods to control the casting content.

For a sample of the cast button, take a look at the [CastVideos-material](https://github.com/googlecast/CastVideos-material) sample.

#Setup
Use [Bower](http://bower.io/) to include the cast-button in your web app.  The following command will add the cast-button and it's dependencies to your project.

bower install --save googlecast/cast-button-polymer

#Integration
The easiest way to integrate is to use one of the already provided elements which contain cast-button.  For a custom integration, you'll need to first include [Polymer](https://www.polymer-project.org/0.5/docs/start/getting-the-code.html).

##Including the element
In your html include the element

    <link rel="import"
        href="bower_components/cast-button-polymer/cast-button-polymer.html">


Add the element to your HTML replacing appId with your receiver appId.

    <cast-button id="button_cast" appId="{{ appId }}" color="white"></cast-button>

##Initializing the element

