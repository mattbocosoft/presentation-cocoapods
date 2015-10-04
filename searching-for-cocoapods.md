#Searching for CocoaPods

As of October 2015, there are more than 12,000 CocoaPods published on the CocoaPods trunk. Each CocoaPod is registered via a Podspec, which is a specification that describes a version of a CocoaPod. Here is the official repository of Podspecs: [https://github.com/CocoaPods/Specs](https://github.com/CocoaPods/Specs)

Below are a variety of options to help you search for and discover new CocoaPods.

##CocoaPods Homepage
The [CocoaPods homepage](https://cocoapods.org) offers a search field to look for CocoaPods by name, version, author, keywords, summary or dependencies. Search results are filtered by the CocoaPods [quality index](https://guides.cocoapods.org/making/quality-indexes) and feature a beautiful new summary interface including a quick way to copy the dependency configuration to the Podfile.

####Quality Index
To help users decide which dependencies to choose, CocoaPods automatically generates a quality index based on a variety of factors including:  
* Popularity  
* Documentation  
* README Complexity  
* CHANGELOG  
* Language Choice (Swift is preferred)  
* Licensing Issues  
* Code Calls (smaller more composable libraries are preferred)  
* Ownership gives preference to official APIs over unofficial  

For more information about the quality index, go here [https://guides.cocoapods.org/making/quality-indexes](https://guides.cocoapods.org/making/quality-indexes)  

##"pod search" command
In the terminal, type <code>'pod search \<query\>'</code> where \<query\> represents the keyword(s) you are searching for.

Use <code>pod search --help</code> for more information.

![pod-search-command](images/pod-search-command.png)  

##CocoaPod RSS Feed
CocoaPods.org offers an RSS Feed to "never miss a pod again!" Subscribe to [https://feeds.cocoapods.org/new-pods.rss](https://feeds.cocoapods.org/new-pods.rss).

##Keep an eye out for Podspecs
CocoaPods is fast becoming the standard method for Cocoa Dependency Management, so most popular libraries support CocoaPods. Look for a Podspec in the root directory of the library or a note about CocoaPod installation in the readme.

##Other sources
Additionally, there are some 3rd-party resources which can help you sift through the almost 12,000 CocoaPods currently available.

* [What the Pod: A ranked list of the most popular CocoaPods](http://www.whatthepod.com)  
* [Search CocoaPods @ Wantedly](http://cocoapods.wantedly.com)  
* [Trending CocoaPods](http://trendingcocoapods.github.io)

**Previous**: [Installing CocoaPods](install-cocoapods.md)  
**Next Up**: [Integrating pods](integrating-pods.md)  
...or return to the [homepage](README.md).
