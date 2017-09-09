
![title](Images/MediaBrowser_w.png)

<p align="center">
  <img alt="Swift" src="https://img.shields.io/badge/Swift-3.1-orange.svg">
  <a href="https://cocoapods.org/pods/MediaBrowser" target="_blank">
    <img alt="CocoaPods" src="http://img.shields.io/cocoapods/v/MediaBrowser.svg">
  </a>
  <a href="https://github.com/younatics/MediaBrowser" target="_blank">
    <img alt="Platform" src="https://img.shields.io/cocoapods/v/MediaBrowser.svg?style=flat">
  </a>
  <a href="http://cocoadocs.org/docsets/MediaBrowser" target="_blank">
    <img alt="CocoaDocs" src="https://img.shields.io/cocoapods/metrics/doc-percent/MediaBrowser.svg">
  </a>
  <a href="https://github.com/Carthage/Carthage" target="_blank">
    <img alt="Carthage" src="https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat">
  </a>
    <a href="(https://github.com/younatics/MediaBrowser/blob/master/LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat">
  </a>
</p>

## Intoduction
🏞 MediaBrowser is written in Swift3, using [SDWebImage](https://github.com/rs/SDWebImage) 4.2.0 version for caching. 

| Single Photo | Multiple Photos And Video |
| ------------- | ------------------------- |
| ![SinglePhoto](Images/SinglePhoto.gif) | ![MultiplePhotosAndVideo](Images/MultiplePhotosAndVideo.gif) |
| Multiple Photo Grid | Multiple Photo Selection |
| ![MultiplePhotoGrid](Images/MultiplePhotoGrid.gif)  | ![PhotoSelection](Images/PhotoSelection.gif)  |
| Web Photos | Web Photos Grid |
| ![WebPhotos](Images/WebPhotos.gif)  | ![WebPhotoGrid](Images/WebPhotoGrid.gif)  |

## Requirements
`MediaBrowser` is written in Swift 3. Compatible with iOS 8.1+

## Installation
### Cocoapods
```ruby
pod 'MediaBrowser'
```
### Carthage
```
github "younatics/MediaBrowser"
```

## Usage
### Basic Usage

Get `MediaBrowser` and set `MediaBrowserDelegate`
```Swift 
let browser = MediaBrowser(delegate: self)
self.navigationController?.pushViewController(browser, animated: true)

//MediaBrowserDelegate
func numberOfMedia(in mediaBrowser: MediaBrowser) -> Int {
  return mediaArray.count
}
    
func media(for mediaBrowser: MediaBrowser, at index: Int) -> Media {
  if index < mediaArray.count {
    return mediaArray[index]
  }
  return DemoData.localMediaPhoto(imageName: "MotionBookIcon", caption: "Photo at index is Wrong")
}
```

## References
#### Please tell me or make pull request if you use this library in your application :) 

## Author
[younatics 🇰🇷](http://younatics.github.io)

## License
MediaBrowser is available under the MIT license. See the LICENSE file for more info.
