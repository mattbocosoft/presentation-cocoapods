# Cocoapods Dependency Manager

CococaPods is a dependency manager for Swift and Objective-C Cocoa projects. CocoaPods handles many workflows automatically that developers would normally need to perform manually, including:  

* Fetching dependency source code
* Recursively resolve and merge dependencies
* Integrate source code, linker flags, library paths, header paths, etc.
* Manage dependency life-cycle
  - Installing new dependencies
  - Updating dependencies
  - Removing dependencies

CocoaPods has become the standard for dependency management, and even [Google embraced it](http://thenextweb.com/insider/2015/05/28/google-is-embracing-cocoapods-to-bring-its-services-to-ios-developers/) as their standard for [delivering their tools](https://cocoapods.org/pods/Google) to iOS developers.

##Development Environment

Cococapods is used exclusively by Cocoa developers (iOS and Mac apps) therefore it can only be used on the Mac OS X operating system and with [Xcode](https://en.wikipedia.org/wiki/Xcode) Integrated Development Environment ([IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)).

CocoaPods is a command-line tool but a basic graphical user-interface exists [as an Xcode Plugin](https://github.com/kattrali/cocoapods-xcode-plugin).

##Consuming CocoaPods
CocoaPods enables software developers to quickly and easily integrate 3rd-party libraries, called Pods.

1. [Installing CocoaPods](install-cocoapods.md)  
2. [Searching for pods](searching-for-cocoapods.md)  
3. [Integrating pods](integrating-pods.md)  

##Producing CocoaPods
Anyone can use CocoaPods to bundle and share their code with other developers.

1. [Creating a Cocoapod](creating-pods.md)  
2. [CocoaPod Distribution](distributing-pods.md)  

Check out these [resources and tutorials for further reading](Further-reading-and-resources.md).  

Written by [Matthew Thomas](mailto:matt@bocosoft.net)  
Fall 2015, CSCI 5828
