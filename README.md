# QT GH DLL Injector

Rebuild of Guided Hacking DLL Injector that works with MSVC2019/MSVC2022 and QT 5.15.2.

## Table of Contents

- [Introduction](#introduction)
- [Screenshot](#screenshot)
- [How to Build](#how-to-build)
- [Features](#features)
- [Credits](#credits)
- [License](#license)

## Introduction

This repository contains a rebuild of the Guided Hacking DLL Injector that is compatible with MSVC2019/MSVC2022 and QT 5.15.2.

## Modified Version

This version is based on a modified version by [multikill](https://github.com/multikill/GH_Injector_MSVC_2019_QT_5_15_0).

## Screenshot

![Screenshot](https://i.gyazo.com/a9347287866c0220f9c09fd8a20ebbe1.png)

## How to Build

1. **Visual Studio 2022**
    - Download and install Visual Studio 2022 from [here](https://visualstudio.microsoft.com/vs/).

2. **QT**
    - Download the QT installer from [here](https://www.qt.io/download-qt-installer).
    - Install QT 5.15.2 for both MSVC 2019 32-bit and 64-bit.

3. **QT VS Tools for Visual Studio 2022**
    - Download the QT VS Tools extension from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=TheQtCompany.QtVisualStudioTools2022).

4. **Static QT 5.15.2**
    - Download the static QT 5.15.2 release from [this repository](https://github.com/martinrotter/qt5-minimalistic-builds/releases).
    - Extract it to "%QTDIR%\5.15.2\qt-5.15.2-static-msvc2019-x86_64".

5. **Setup MSVC**
    - In Visual Studio, go to `Toolbar -> QT VS Tools -> QT Options -> Add` and add the following paths:
        - "%QTDIR%\5.15.2\msvc2019"
        - "%QTDIR%\5.15.2\msvc2019_64"
        - "%QTDIR%\5.15.2\qt-5.15.2-static-msvc2019-x86_64"
    - Go to `Toolbar -> Project -> Properties -> QT Project Settings -> QT Installation` and set the installations for different architectures:
        - x86 -> msvc2019
        - x64 -> msvc2019_64
        - x64_static -> qt-5.15.2-static-msvc2019-x86_64
    - Restart Visual Studio to repair intellisense and then build the project.

6. **GH Injector-Library**
    - Download the GH Injector Library from [here](https://github.com/Broihon/GH-Injector-Library).
    - Change the C++ Language to std:c++20.
    - Build the library and copy it to the project folder.

## Features

- Intelligent drag and drop that bypasses UIPI.
- Commandline interface.
- Shortcut generator.
- Auto injection.

## Credits

- [Guided Hacking](https://guidedhacking.com/resources/guided-hacking-dll-injector.4/)
- [Qt Frameless Window DarkStyle](https://github.com/Jorgen-VikingGod/Qt-Frameless-Window-DarkStyle)
- [Qt5 MSVC Static](https://github.com/fpoussin/Qt5-MSVC-Static)

## License

All original licenses of the used components Qt are respected, with the additional exception that compiling, linking, or using is allowed. Refer to the Qt website for License information.
