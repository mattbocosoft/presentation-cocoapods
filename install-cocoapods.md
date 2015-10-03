#Install CocoaPods

##Install
CocoaPods should be installed using Ruby, which comes pre-installed on Mac OS X. Run the following command at the terminal.  

```sudo gem install cocoapods```  

Next you need to setup CocoaPods, which downloads a copy of the official public Podspec [trunk](https://github.com/CocoaPods/Specs) repository to your computer.

```pod setup``` 

The repository now has over 11,000 Podspecs, with more being added each day, so this process could take a while.

##Update
CocoaPods is an open-source project in active-development and updates are frequently released. To make sure you are running the latest version of CocoaPods, you can update via Ruby Gems.  
```sudo gem update cocoapods```

##Xcode Plugin
If you prefer to interact with CocoaPods using a GUI instead of the terminal, there is an Xcode Plugin which adds a few common CocoaPods commands to a menu in Xcode. The plugin is open-source and [available on GitHub](https://github.com/kattrali/cocoapods-xcode-plugin).

![XcodePlugin](https://github.com/kattrali/cocoadocs-xcode-plugin/raw/master/menu.png)

##CocoaPods App
Development has recently begun () on a stand-alone app which will eventually provide full-feature support, but currently only provides very basic commands similar to the Xcode Plugin.

**Next Up**: [Searching for pods](searching-for-cocoapods.md)  
...or return to the [homepage](README.md).
