# FaceRecOfflineSDK

![Cocoapods](https://img.shields.io/cocoapods/v/FaceRecOfflineSDK)
![Swift 5.0](https://img.shields.io/badge/Swift-5.0-orange.svg)
![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20watchOS%20%7C%20tvOS-lightgrey.svg)
[![Licence](https://img.shields.io/cocoapods/l/LivenessSDK?color=red&logo=red)](https://img.shields.io/cocoapods/l/LivenessSDK?color=red&logo=red)


# iOS Offline Face Recognition (written in Swift).

## Introduction
Brought to you by FaceX.io, this iOS SDK can now be used to integrate on-device Face Recognition into your iOS applications.

## 📑 Index
* [Usage](#usage)
    * [Camera](#camera)
    * [Delegate](#delegate)
* [Version Compatibility](#version-compatibility)
* [Installation](#-installation)
  * [Cocoapods](#using-cocoapods)
* [Contact](#contact)


## Usage

```swift
    let faceRec = FaceRecOffline()
do {

    let result = try faceRec.process(on: "YOUR IMAGE"!)
    let searchResult = try faceRec.search(with: "YOUR IMAGE", in: [ARRAY])

} catch _ {
    print("Something went wrong :(")
}
```
### Camera
For a better image for processing.

```swift

    faceRec.delegate = self
    faceRec.openCamera()
    
```
### Delegate
UICameraCaptureDelegate

```swift

    func cameraController(cameraController: UIViewController, didFinishCapture image:UIImage){
    }
  
    func cameraControllerDidCancel(cameraController: UIViewController){
     }

```

## Version Compatibility

Current Swift compatibility breakdown:

| Swift Version | Framework Version |
| ------------- | ----------------- |
| 5.0           | 1.x               |

[all releases]: https://github.com/friendlynandy/FaceRecOfflineSDK/releases

## Installation

#### CocoaPods

Add the following line to your Podfile.

```
pod "FaceRecOfflineSDK"
```

Then run `pod install` with CocoaPods 0.36 or newer.

## Contact

Feel free to get in touch.

* Website: <https://facex.io>
* Twitter: [@Facex](http://twitter.com/facex)
