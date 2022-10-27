# 已将其适配到支持ffmpeg 5.1.2

# FFmpeg iOS build script

See the following repository for Swift package, .xcframeworks and more:

https://github.com/kewlbear/FFmpeg-iOS

[![Build Status](https://travis-ci.org/kewlbear/FFmpeg-iOS-build-script.svg?branch=master)](https://travis-ci.org/kewlbear/FFmpeg-iOS-build-script)

This is a shell script to build FFmpeg libraries for iOS and tvOS apps.

Tested with:

* FFmpeg 5.1.2
* Xcode 12.2

## Requirements

* https://github.com/libav/gas-preprocessor
* yasm 1.2.0

## Usage

Use build-ffmpeg-tvos.sh for tvOS.

* To build everything:

        ./build-ffmpeg.sh

* To build arm64 libraries:

        ./build-ffmpeg.sh arm64

* To build fat libraries for arm64 and x86_64 (64-bit simulator):

        ./build-ffmpeg.sh arm64 x86_64

* To build fat libraries from separately built thin libraries:

        ./build-ffmpeg.sh lipo

## External libraries

You should link your app with

* libz.dylib
* libbz2.dylib
* libiconv.dylib
