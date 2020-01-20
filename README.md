
<img src="https://github.com/vijayendra-tripathi/AnyDataCache/blob/master/Assets/AnyDataCache.jpg?raw=true" width="600">

<p>&nbsp;</p>

![Swift Version](https://img.shields.io/badge/Swift-5-orange.svg)
[![Version](https://img.shields.io/cocoapods/v/AnyDataCache.svg?style=flat)](http://cocoapods.org/pods/AnyDataCache)
[![License](https://img.shields.io/cocoapods/l/AnyDataCache.svg?style=flat)](http://cocoapods.org/pods/AnyDataCache)
[![Platform](https://img.shields.io/cocoapods/p/AnyDataCache.svg?style=flat)](http://cocoapods.org/pods/AnyDataCache)

# AnyDataCache
 A simple data caching framework based on Realm database.
 
 ## Features

-  [x] Add data with one line of code.
 - [x] Set expiry time and framework will automatically delete data after expiry time.
 - [x] Set disk usage limit and framework will automatically delete old files.
 - [x] Set auto delete property to let framework delete a data only on your instruction.
 - [x] Works on all screens and devices supporting iOS 10.0+
 
 ## CocoaPods

 PopupDialog is available through [CocoaPods](http://cocoapods.org). Simply add the following to your Podfile:

 ```ruby
 use_frameworks!

 target '<Your Target Name>'
 pod 'AnyDataCache'
 ```
 
 <p>&nbsp;</p>

 # Example Usage
 
 Following code can be used to save data into disk -
 
 ```swift
 
 DataCache.sharedInstance.addData(dataKey: dataKey, data: yourData)
 
 ```
 DataKey can be a URL or things like Social Identity (like facebook graph user id)
 Data is a 'Data' object to be saved.
 
 To read back saved data, you can use following code -
 
 ```swift
 
 // Assuming you saved a string as data into DataCache. Response
 // comes back on main thread after a read operation.
 
 DataCache.sharedInstance.getData(dataKey: dataKey) { [weak self] data in
     if let messageData = data?.data {
         if let message = String(data: messageData, encoding: .utf8) {
            print("Your saved message is : \(message)")
         }
     }
 }
 
 ```
 
 # Author

Vijayendra Tripathi, vijayendra.t.inbox@gmail.com
To follow on Twitter:  [@vijayendra_t](https://twitter.com/vijayendra_t)

<p>&nbsp;</p>

# License

PopupDialog is available under the MIT license. See the LICENSE file for more info.

<p>&nbsp;</p>

#### Logo resource credits

Floppy icon: Icons made by <a href="https://www.flaticon.com/authors/flat-icons" title="Flat Icons">Flat Icons</a> from <a href="https://www.flaticon.com/" title="Flaticon"> www.flaticon.com</a>

Orbiton Font - https://fonts.google.com/specimen/Orbitron
