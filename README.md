- [mruac's xml ad dismisser](#mruacs-xml-ad-dismisser)
    - [Features](#features)
    - [License](#license)
    - [Requirements](#requirements)
    - [Supported ad networks](#supported-ad-networks)
    - [Screenshots / Demo](#screenshots--demo)
        - [video demonstration of "app lock" and automatic trigger of ad dismisser](#video-demonstration-of-app-lock-and-automatic-trigger-of-ad-dismisser)
        - ["app lock" macro](#app-lock-macro)
        - [ad dismisser macro](#ad-dismisser-macro)
        - [Llamalab Automate inspect layout flow](#llamalab-automate-inspect-layout-flow)
        - [Capture tool macro](#capture-tool-macro)
    - [Changelog](#changelog)

# mruac's xml ad dismisser

Identifies the appropriate coordinates to tap on, from the xml representation of an advertisement's view layout on an Android system.

This may be suitable for those where image recognition is unreliable.

## Features

* Determines the location of the close / skip / continue button on an ad overlay
* Pins app to prevent unwanted app opens (installed advertised app, app store, web browser)
* Automatically presses back button if out of pinned app
* Automatically relaunches pinned app if no ad detected after some time. (option to disable this supported)

## License

This code is provided under the GNU GPL-3 license.

## Requirements

* Macrodroid with [Javascript code action](https://www.macrodroidforum.com/wiki/index.php/Action:_JavaScript_Code) (version  5.53.6+)
* Llamalab Automate with [Inspect Layout block](https://llamalab.com/automate/doc/block/inspect_layout.html)
* Relevant permissions enabled (Automate and Macrodroid will ask accordingly) - Mainly the Android accessibility service be enabled and permission granted
* Ability to execute adb commands on Macrodroid with root access or Shizuku enabled.

## Supported ad networks

As this is provided without warranty, there is no guarantee that this code may work straight away due to updated layout since last update, or an advertisement layout has not been coded for.

* Pangle
* Mintegral
* Meta / Facebook
* InMobi
* Supersonic
* Unity
* Google
* Chartboost
* HyperMX
* Verve SSP
* InnerActive
* Bigo

If a specific layout is not detected, it will attempt to identify the close buttons in top right or top left corners.

## Screenshots / Demo

### video demonstration of "app lock" and automatic trigger of ad dismisser

<video controls src="media/demo.mp4" title="alt text"></video>

### "app lock" macro

![alt text](<media/macrodroid app lock and auto trigger ad dismisser.png>)

### ad dismisser macro

![alt text](<media/macrodroid dismisser macro.png>)

### Llamalab Automate inspect layout flow

![alt text](<media/llamalab automate flow.png>)

### Capture tool macro

![alt text](<media/macrodroid capture tool macro.png>)

## Changelog

* 20250627: initial public release
