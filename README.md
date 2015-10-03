# Cocoapods Dependency Manager

CococaPods is a dependency manager for Swift and Objective-C Cocoa projects. CocoaPods has become the standard for dependency management, and even [Google has embraced it](http://thenextweb.com/insider/2015/05/28/google-is-embracing-cocoapods-to-bring-its-services-to-ios-developers/) as their standard for [delivering their tools](https://cocoapods.org/pods/Google) to iOS developers. CocoaPods is a must-have tool for both iOS and OS X developers. There are currently (*as of October 2015*) more than 12,000 CocoaPods available for consumption.

##Advantages of CocoaPods

CocoaPods handles many workflows automatically that developers would normally need to perform manually, including:  

Without dependency management, developers have to find, download, integrate and manage their dependencies manually. This includes adding the right files in the right places, linker flags, and any dependencies of those libraries. In the future if the developer no longer needs that library, they'll have a tougher time tearing down and remembering, for example, which linker flags can be removed without breaking their other libraries.

* Fetching dependency source code
* Recursively resolve and merge dependencies
* Integrate source code, linker flags, library paths, header paths, etc.
* Manage dependency life-cycle
  - Installing new dependencies
  - Updating dependencies
  - Removing dependencies

Other forms of dependency management, like git submodules, are specific to source control. Consuming CocoaPods on the other hands works well across different types of source control (Git, SVN, Mercurial) or not at all.

##Disadvantages of CocoaPods

It's important to also be aware of what you are losing as a developer by using CocoaPods instead of its alternatives. In my experience, the biggest drawback of CocoaPods as a consumer is the loss of control over dependency content. If the dependency is a black-box library (*.a) instead of an open-source library, then the developer never had this control in the first place.

####Modifying Pod Content within Context
When there is a bug in a Pod, you can't just modify the Pod in context without a bit of work.  

1. Find the CocoaPod on Github and fork your own version.
2. Point your local Podfile to the latest commit on your new fork instead of the default CocoaPod trunk.
    ```pod '[POD_NAME]', :git => 'https://github.com/[USERNAME]/[POD_NAME].git', :head```
3. Run ```pod install``` again to update the changes

Now you are able to make changes in your own fork of the repo and have them reflected in your consuming project. If you want the latest changes from the official CocoaPod, then you'll have to rebase your changes or send a pull-request to the author with your bug-fix.

####Viewing Pod History

When working on a library locally or from within the context of your project, you can view the entire history of that project. When you install a CocoaPod however, only the latest version of the code is fetched and integrated into your project. Like modifying pods, there is a way of remedying this with a bit of work.

1. Clone or fork the CocoaPod dependency repo and pull it to your machine.
2. Move the repo inside your project repo and add it as a git submodule.
3. Point your local Podfile to the latest commit on your new fork instead of the default CocoaPod trunk.
    ```pod '[POD_NAME]', :path => '[POD_NAME]'``` (By default, path is relative to project root)
4. Run ```pod install``` again to update the changes.

##Development Environment

Cococapods is used exclusively by Cocoa developers (iOS and Mac apps) therefore it can only be used on the Mac OS X operating system and with [Xcode](https://en.wikipedia.org/wiki/Xcode) Integrated Development Environment ([IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)).

CocoaPods is a command-line tool but a basic graphical user-interface exists [as an Xcode Plugin](https://github.com/kattrali/cocoapods-xcode-plugin).

CocoaPods supports Git, SVN, and Mercurial source control however for the sake of this presentation, I will only be using Git.

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
