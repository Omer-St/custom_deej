# deej

Custom deej is an hardware volume mixer for Windows.
It lets you use real-life sliders, potentiometers, buttons, small screen and led lights to seamlessly control the volumes of different apps, and In-App (such as your music player, the game you're playing and your voice chat session) without having to stop what you're doing.

The fork is from [deej](https://github.com/omriharel/deej) by Omeri Harel, you should start there.

## Table of contents

- [Features](#features)
- [Hardware](#hardware)
- [Software](#software)
  -- [Arduiuno C Code](#arduino)
  -- [Windows Go Code](#arduino)
- [How to run](#how-to-run)

### Features

This Fork contain few more features then the starndard [deej](https://github.com/omriharel/deej) :

- Support sliders, potentiometers as deej
- Support buttons to toggle Mute/Un-Mute
- Support small screen to display names and levels
- Support led lights indecation for Mute/Un-mute

### Hardware

- Arduino, connected to the each of the following, up to user to decide what and amount
  
### Software

#### Arduino

- The code running on the Arduino board is a [C program](./arduino/deej-5-sliders-vanilla/deej-5-sliders-vanilla.ino) ,Its need to be adjusted to your Hardware

#### Windows

- The PC runs a lightweight [Go client](./pkg/deej/cmd/main.go) in the background. This client reads the serial stream and adjusts app volumes according to the given configuration file

## How to run

deej uses a simple YAML-formatted configuration file named [`config.yaml`](./config.yaml), placed alongside the deej executable.

The config file determines which applications (and devices) are mapped to which sliders, and which parameters to use for the connection to the Arduino board, as well as other user preferences.

**This file auto-reloads when its contents are changed, so you can change application mappings on-the-fly without restarting deej.**

## License

deej is released under the [MIT license](./LICENSE).
