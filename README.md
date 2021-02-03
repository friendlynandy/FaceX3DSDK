# FaceX3DSDK

![Cocoapods](https://img.shields.io/cocoapods/v/FaceX3DSDK)
![Swift 5.0](https://img.shields.io/badge/Swift-5.0-orange.svg)
![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20watchOS%20%7C%20tvOS-lightgrey.svg)
[![Licence](https://img.shields.io/cocoapods/l/FaceX3DSDK?color=red&logo=red)](https://img.shields.io/cocoapods/l/FaceX3DSDK?color=red&logo=red)

## Introduction
3D Face reconstruction using just mobile camera.(written in Swift)

## Index
* [Usage](#usage)
    * [Camera](#camera)
    * [Delegate](#delegate)
* [Version Compatibility](#version-compatibility)
* [Installation](#installation)
  * [Manual](#manual)
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
### Manual installation

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


## Contact

Feel free to get in touch.

* Website: <https://facex.io>
* Twitter: [@Facex](http://twitter.com/facex)
