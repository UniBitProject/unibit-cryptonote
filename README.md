# UniBitX App
## https://unibitx.app/

  
   _/    _/  _/      _/  _/_/_/  _/_/_/    _/_/_/  _/_/_/_/_/  _/      _/    
  _/    _/  _/_/    _/    _/    _/    _/    _/        _/        _/  _/       
 _/    _/  _/  _/  _/    _/    _/_/_/      _/        _/          _/          
_/    _/  _/    _/_/    _/    _/    _/    _/        _/        _/  _/         
 _/_/    _/      _/  _/_/_/  _/_/_/    _/_/_/      _/      _/      _/        

 UniBitX v0.1.1.1286

#### Master Branch Build Status
[![Build Status](https://travis-ci.org/turtlecoin/turtlecoin.svg?branch=master)](https://travis-ci.org/turtlecoin/turtlecoin) [![Build status](https://ci.appveyor.com/api/projects/status/github/turtlecoin/turtlecoin?branch=master&svg=true)](https://ci.appveyor.com/project/RocksteadyTC/turtlecoin)

#### Development Branch Build Status
[![Build Status](https://travis-ci.org/turtlecoin/turtlecoin.svg?branch=development)](https://travis-ci.org/turtlecoin/turtlecoin) [![Build status](https://ci.appveyor.com/api/projects/status/github/turtlecoin/turtlecoin?branch=development&svg=true)](https://ci.appveyor.com/project/RocksteadyTC/turtlecoin)

![image](https://avatars3.githubusercontent.com/u/31015318?s=460&v=4)

### Installing

We offer the latest releases here: https://latest.unibitx.org
If you would like to compile from source code yourself, read on.

### How To Compile

#### Linux

##### Prerequisites

You will need the following packages: [Boost](https://www.boost.org/), [OpenSSL](https://www.openssl.org/), cmake (3.8 or higher), make, and git.

You will also need either GCC/G++, or Clang.

If you are using GCC, you will need GCC-7.0 or higher.

If you are using Clang, you will need Clang 6.0 or higher. You will also need libstdc++\-6.0 or higher.

##### Generic Linux

Ensure you have the dependencies listed above.

If you want to use clang, ensure you set the environment variables `CC` and `CXX`.
See the ubuntu instructions for an example.

- `git clone -b master --single-branch https://github.com/unibitx/unibitx`
- `cd UniBitX`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./UniBitXd --version`


#### OSX/Apple 

##### Prerequisites

- Install XCode and Developer Tools.

##### Building

- `which brew || /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- `brew install --force cmake boost llvm openssl`
- `export CC=/usr/local/opt/llvm/bin/clang`
- `export CXX=/usr/local/opt/llvm/bin/clang++`
- `git clone -b master --single-branch https://github.com/unibitx/unibitx`
- `cd unibitx`
- `mkdir build`
- `cd build`
- `cmake .. -DBoost_NO_BOOST_CMAKE=TRUE`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./UniBitXd --version`


#### Windows

##### Prerequisites

You can build for 32-bit or 64-bit Windows. **If you're not sure, pick 64-bit.**

- Install [Visual Studio 2017 Community Edition](https://www.visualstudio.com/thank-you-downloading-visual-studio/?sku=Community&rel=15&page=inlineinstall)
- When installing Visual Studio, it is **required** that you install **Desktop development with C++**
- Install the latest version of Boost (currently Boost 1.68). Select the appropriate version for your system:
  - [Boost 64-bit](https://bintray.com/boostorg/release/download_file?file_path=1.68.0%2Fbinaries%2Fboost_1_68_0-msvc-14.1-64.exe)
  - [Boost 32-bit](https://bintray.com/boostorg/release/download_file?file_path=1.68.0%2Fbinaries%2Fboost_1_68_0-msvc-14.1-32.exe)
- Install the latest full version of OpenSSL (currently OpenSSL 1.1.1b). Select the appropriate version for your system:
  - [OpenSSL 64-bit](https://slproweb.com/download/Win64OpenSSL-1_1_1b.exe)
  - [OpenSSL 32-bit](https://slproweb.com/download/Win32OpenSSL-1_1_1b.exe)

##### Building

For 64-bit:
- From the start menu, open 'x64 Native Tools Command Prompt for vs2017'.
- `cd <your_unibitx_directory>`
- `mkdir build`
- `cd build`
- `set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%`
- `cmake -G "Visual Studio 15 2017 Win64" .. -DBOOST_ROOT=C:/local/boost_1_68_0`
- `MSBuild UniBitX.sln /p:Configuration=Release /m`

For 32-bit:
- From the start menu, open 'x86 Native Tools Command Prompt for vs2017'.
- `cd <your_unibitx_directory>`
- `mkdir build`
- `cd build`
- `set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%`
- `cmake -G "Visual Studio 15 2017" .. -DBOOST_ROOT=C:/local/boost_1_68_0`
- `MSBuild UniBitX.sln /p:Configuration=Release /p:Platform=Win32 /m`

The binaries will be in the `src/Release` folder when you are complete.

- `cd src`
- `cd Release`
- `UniBitXd.exe --version`

#### Thanks
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, TurtleCoin Community, Universal Bit Project

### Copypasta for license when editing files

Hi UniBitX contributor, thanks for forking and sending back Pull Requests. Extensive docs about contributing are in the works or elsewhere. For now this is the bit we need to get into all the files we touch. Please add it to the top of the files, see [src/CryptoNoteConfig.h]() for an example.

```
// Copyright (c) 2012-2017, The CryptoNote developers, The Bytecoin developers
// Copyright (c) 2014-2018, The Monero Project
// Copyright (c) 2018-2019, The TurtleCoin Developers
// Copyright (c) 2018-2019, The Universal Bit Project
//
// Please see the included LICENSE file for more information.
```
