#Removing CocoaPods
If you no longer need to use CocoaPods in your proejct, you can remove it by first deleting the relevant files and folder from your project:  

* Pods  
* Podfile  
* Podfile.lock  

####Remove from a Workspace (Default)
If the workspace file was created automatically by CocoaPods, you can delete it too and go back to using just the project file. Remove the Pods project if you are still using the workspace.

####Remove from a Project
If you specified the "--no-integrate" flag when first installing your Pod dependencies, then you will need to manually remove the CocoaPod references from the project. To do this, follow these steps:  

1. Remove the config files  
  * Pods-[PROJECT_NAME].([CONFIGURATION].).xcconfig  
2. Remove the Pods library  
  * libPods-[PROJECT_NAME].a  
3. In the Target Build Phases, delete...  
  * "Check Pods Manifest.lock"  
  * "Copy Pods Resources section"  

Alternatively, there is an open-source utility (not available as a CocoaPod) that can be used at your own risk. That library is available here, [cocoapods-deintegrate](https://github.com/kylef/cocoapods-deintegrate).

**Previous**: [Challenges with CocoaPods](cocoapod-challenges.md)  
**Next Up**: [Creating CocoaPods](creating-pods.md)  
...or return to the [homepage](README.md).
