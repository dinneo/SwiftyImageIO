# SwiftyImageIO

[![Swift](https://img.shields.io/badge/Swift-3.0-orange.svg)]()
[![Build Status](https://travis-ci.org/diejmon/SwiftyImageIO.svg?branch=master)](https://travis-ci.org/diejmon/SwiftyImageIO)
[![Version](https://img.shields.io/cocoapods/v/SwiftyImageIO.svg?style=flat)](http://cocoapods.org/pods/SwiftyImageIO)
[![License](https://img.shields.io/cocoapods/l/SwiftyImageIO.svg?style=flat)](http://cocoapods.org/pods/SwiftyImageIO)
[![Platform](https://img.shields.io/cocoapods/p/SwiftyImageIO.svg?style=flat)](http://cocoapods.org/pods/SwiftyImageIO)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![codebeat badge](https://codebeat.co/badges/e67c5860-b3fd-4c7a-b825-cd698f13a3ad)](https://codebeat.co/projects/github-com-diejmon-swiftyimageio)


Swift wrapper around ImageIO framework.

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Examples


### Create image thumbnail

```swift
import SwiftyImageIO

let source = ImageSource(data: imageData, options: nil)
let thumbnailCGImage = source?.createThumbnail(maxPixelSize: thumbnailSize)
```

### Write image to disk

```swift
import SwiftyImageIO
import MobileCoreServices

if let imageDestination = ImageDestination(url: saveURL, UTI: kUTTypeJPEG, imageCount: 1) {
  imageDestination.addImage(cgImage)
  let imageSaved = imageDestination.finalize()
}
```

## Requirements

## Installation

SwiftyImageIO is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "SwiftyImageIO"
```

## Author

Alexander Belyavskiy, diejmon@gmail.com

## License

SwiftyImageIO is available under the MIT license. See the LICENSE file for more info.
