#Install CocoaPods

##Install
CocoaPods should be installed using Ruby, which comes pre-installed on Mac OS X. Run the following command at the terminal to install CocoaPods.  

```sudo gem install cocoapods```  

The command line should show something like this:  

![install-cocoapods](images/install-cocoapods.png)  

Next you need to setup the CocoaPods installation, which includes downloading a copy of the official public Podspec [trunk](https://github.com/CocoaPods/Specs) repository to your computer.

```pod setup``` 

The repository now has over 12,000 Podspecs with more being added each day, so this process could take some time.

##Update
CocoaPods is an open-source project in active-development and updates are frequently released. To make sure you are running the latest version of CocoaPods, you can update via Ruby Gems.  

```$ [sudo] gem update cocoapods```  

When you are using CocoaPods, keep an eye out for messages on the command line alerting you of new updates.  

> CocoaPods 0.39.0.beta.5 is available.  
> To update use: `gem install cocoapods --pre`  
> [!] This is a test version we'd love you to try.  
  
> For more information see http://blog.cocoapods.org  
> and the CHANGELOG for this version http://git.io/BaH8pQ.  

If you want to use a pre-release version of CocoaPods, then you can run this command:  

```$ [sudo] gem install cocoapods --pre```    

##Xcode Plugin
If you prefer to interact with CocoaPods using a GUI instead of the terminal, there is an Xcode Plugin which adds a few common CocoaPods commands to a menu in Xcode. The plugin is open-source and [available on GitHub](https://github.com/kattrali/cocoapods-xcode-plugin).

![XcodePlugin](https://github.com/kattrali/cocoadocs-xcode-plugin/raw/master/menu.png)

##CocoaPods App
Development has recently begun on a stand-alone app which will eventually provide full-feature support, but currently only provides very basic commands similar to the Xcode Plugin. This will allow developers to install CocoaPods without Ruby Gems or Homebrew. Check out the website here [https://github.com/CocoaPods/CocoaPods-app](https://github.com/CocoaPods/CocoaPods-app).  

**Next Up**: [Searching for pods](searching-for-cocoapods.md)  
...or return to the [homepage](README.md).
