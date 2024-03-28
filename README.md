# Custom deej

Custom deej is an hardware volume mixer for Windows.
It lets you use real-life sliders, potentiometers, buttons, small screen and led lights to seamlessly control the volumes of different apps, and In-App (such as your music player, the game you're playing and your voice chat session) without having to stop what you're doing.

The fork is from [deej](https://github.com/omriharel/deej) by Omeri Harel, you should start there.

## Table of contents

- [Features](#features)
- [Hardware](#hardware)
- [Software](#software)
- [License](#license)

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

- The code running on the Arduino board is a [C program](./arduino/deej-5-sliders-vanilla/deej-5-sliders-vanilla.ino) , and is using the configuration in first segment of the file.

#### Windows

- The PC runs a [Go client](./pkg/deej/cmd/main.go) in the background, and its using YAML-formatted configuration file named config.yaml. 

### License

[deej](https://github.com/omriharel/deej) is released under the [MIT license](./LICENSE).
[custpm deej](https://github.com/Omer-St/custom_deej) is released under the [MIT license](./LICENSE).
