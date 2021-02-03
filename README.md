# FaceX3DSDK

![Swift 5.0](https://img.shields.io/badge/Swift-5.0-orange.svg)
![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20watchOS%20%7C%20tvOS-lightgrey.svg)
[![Licence](https://img.shields.io/cocoapods/l/FaceX3DSDK?color=red&logo=red)](https://img.shields.io/cocoapods/l/FaceX3DSDK?color=red&logo=red)

## Introduction
3D Face reconstruction using just mobile camera.(written in Swift)

## Index
* [Usage](#usage)
    * [Delegate](#delegate)
* [Version Compatibility](#version-compatibility)
* [Installation](#installation)
  * [Manual](#manual)
  * [Update Info.plist](#update-infoplist)
* [Customization](#customization)
   * [Steps](#steps)
   * [Thresholds](#thresholds)
* [Localization Strings](#localization-strings)
* [Contact](#contact)


## Usage

```swift
    let faceX3D = FaceX3DSDK()
    
   //Delegates for successful 3d files creation and errors if any
   faceX3D.delegate = self
   
   //Start camera for capturing images with on screen directions
   faceX3D.start3DImaging()


```
### Delegate
FaceX3DDelegate

```swift

    func didCreate3DObject(objectAt url: URL){
    //url of the 3D .obj file created
     }
  
    func didFailWithError(error: Error){
   
     }

```

## Version Compatibility

Current Swift compatibility breakdown:

| Swift Version | Framework Version |
| ------------- | ----------------- |
| 5.0           | 1.x               |

[all releases]: https://github.com/friendlynandy/FaceX3DSDK/releases

## Installation
### Manual

You will be required to do few steps:

Download FaceX3DSDK.framework and copy it into `Embedded Binaries` section. Don't forget to select `Copy items if needed`.

Now you can import your dependencies e.g.:

ObjC:
```objective-c
@import FaceX3DSDK;
```
Swift:
```swift
import FaceX3DSDK
```

### Update Info.plist

In order to use camera, you need to have `NSCameraUsageDescription`
entries in your `Info.plist`.

These entries are required by Apple. User will be prompted for the Camera usage permissions with your provided text only when he tries to use the camera.

`NSCameraUsageDescription` - When user tries to use Camera


## Customization

You can set some properties for FaceX3DSDK.

### Steps
| Steps | Value | Default | 
| ------- | ------- |------- | 
| **API Base URL**(baseURL)  | `String` | `...` | 
| **Face outline border with face**(faceFoundBorderColor)   | `cgColor` | `UIColor.red.cgColor` | 
| **Face outline border without face**(faceNotFoundBorderColor)   | `cgColor` | `UIColor.gray.cgColor` | 
| **Progress bar right color**(rightProgressColor)   | `UIColor` | `UIColor.white` | 
| **Progress bar left color**(leftProgressColor)   | `UIColor` | `UIColor.blue` | 
| **Face outline border width**(borderWidth)   | `CGFloat` | `4` | 
| **Face outline image**(facwOutlineImage)   | `UIImage` | `UIImage(named: "faceOutline")` | 




### Thresholds
| Property | Default | 
| ------- | ------- | 
| **Max left yaw**(maxLeftYaw)  | `-0.30` | 
| **Max right yaw**(maxRightYaw)  | `0.35` | 
| **Min left yaw**(minLeftYaw)  | `-0.35` | 
| **min right yaw**(minRightYaw)  | `0.30` | 

## Localization Strings
Add these strings to your respected Localization.Strings language file

```
"Please blink your eyes"
"Please open your mouth"
"Please turn your face to right and left"
"Thank You"
"No face Detected"
"Perfect"
"Please bring your face inside face outline above"

```


## 📋 Supported OS & SDK Versions
* iOS 12.0+
* iPadOS 13.0+
* Swift 5

## Contact

Feel free to get in touch.

* Website: <https://facex.io>
* Twitter: [@Facex](http://twitter.com/facex)
