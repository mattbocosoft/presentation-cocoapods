![cocoapods-logo](images/cocoapods-logo.png)
# CocoaPods Dependency Manager

CococaPods is a dependency manager for Swift and Objective-C Cocoa projects. CocoaPods is officially still in beta however it has already become the standard for dependency management for Cocoa, and even [Google has embraced it](http://thenextweb.com/insider/2015/05/28/google-is-embracing-cocoapods-to-bring-its-services-to-ios-developers/) as their standard for [delivering their tools](https://cocoapods.org/pods/Google) to iOS developers.  

CocoaPods is a free open-source tool created by a community of developers who "get pleasure from working on something that can improve [their] small piece of the universe, [without expecting any financial gains](https://blog.cocoapods.org/Why-we-dont-accept-donations/)." [According to Wikipedia](https://en.wikipedia.org/wiki/CocoaPods), Eloy Durán and Fabio Pelosin, inspired by RubyGems and Bundler, started work on CocoaPods in late 2011 and publicly released the first version on September 1, 2011.

CocoaPods is a must-have tool for both iOS and OS X developers. As of October 2015, there are more than 12,000 CocoaPods available for use.  

##Advantages of using CocoaPods

CocoaPods handles many workflows automatically that developers would normally need to perform manually, including:  

* Fetching dependency source code
* Recursively resolve and merge dependencies
* Integrate source code, linker flags, library paths, header paths, etc.
* Manage dependency life-cycle
  - Installing new dependencies
  - Updating dependencies
  - Removing dependencies

Without dependency management, developers have to find, download, integrate and manage their dependencies manually. This includes adding the right files in the right places, linker flags, and any dependencies of those libraries. In the future if the developer no longer needs that library, they'll have a tougher time tearing down and remembering, for example, which linker flags can be removed without breaking their other libraries.  

Other forms of dependency management, like git submodules, are specific to source control. Consuming CocoaPods on the other hands works well across different types of source control (Git, SVN, Mercurial) or not at all.  

##Development Environment

Cococapods is used exclusively by Cocoa developers (iOS and Mac apps) therefore it can only be used on the Mac OS X operating system with the [Xcode](https://en.wikipedia.org/wiki/Xcode) Integrated Development Environment ([IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)).

CocoaPods is a command-line tool but a basic graphical user-interface exists [as an Xcode Plugin](https://github.com/kattrali/cocoapods-xcode-plugin).

CocoaPods supports Git, SVN, and Mercurial source control. This presentation assumes that the reader is running Mac OS X, Xcode and using Git.

##Consuming CocoaPods
Assuming an already functional environment, it takes just minutes to get up and running with CocoaPods. CocoaPods enables software developers to quickly and easily integrate 3rd-party libraries, called Pods for short. Follow these steps to get going:  

1. [Installing CocoaPods](install-cocoapods.md)  
2. [Searching for pods](searching-for-cocoapods.md)  
3. [Integrating pods](integrating-pods.md)  
4. [Challenges with CocoaPods](cocoapod-challenges.md)

##Producing CocoaPods
Anyone can use CocoaPods to bundle and share their code with other developers both publicly and privately. Follow these steps to create your own CocoaPod:  

1. [Creating a Cocoapod](creating-pods.md)  
2. [CocoaPod Distribution](distributing-pods.md)  

If you are both the producer and the consumer of a library of source code, then wrapping your library in a Pod adds  overhead that should be justified. If others are using your library or contributing, then that is justification enough, but if no one outside of your group will be using for the forseeable future, you may want to wait before wrapping it in a CocoaPod at least until continuous active development has slowed down.  

Check out these [resources and tutorials for further reading](Further-reading-and-resources.md).  

Written by [Matthew Thomas](mailto:matt@bocosoft.net)  
Fall 2015, CSCI 5828
