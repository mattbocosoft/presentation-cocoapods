#Integrating Pods

By default, CocoaPods use Xcode workspaces instead of Xcode projects. So before you do anything, close the Xcode project you are working in.  

##Create the Podfile
At the terminal, <code>cd</code> into the root directory of your project. You will need to create a file called **'Podfile'** (with no file-type extension). This can be done manually (<code>touch Podfile</code>) or by running the command <code>pod init</code>.  

**'Podfile'** will act as your project's CocoaPod configuration. Here you will specify your project settings and dependencies. For now we can leave this blank.

##Set-up the workspace
Now that you have a **'Podfile'** in place, run <code>pod install</code> at the terminal to generate the project workspace. From now on, open up the workspace file instead of the project file.

When you open up the workspace file in Xcode, you should now see two sub-projects in the workspace. Expand the **Pods** workspace to reveal that the **'Podfile'** has been referenced. Click on **'Podfile'** to begin editing it. Define the project platform on the first line of the file. For a project targeting iOS, this would be:  
<code>platform :ios, "7.0"</code>

Next you can begin adding project dependencies.

##Define project dependencies
Once you've [found](searching-for-cocoapods.md) a CocoaPod you'd like to integrate, add it to the Podfile using its name.

*Integrate the latest version of RestKit*  
```pod 'RestKit'```  

The Podfile can have many dependencies. Each pod should be placed on its own line.

##Specifying dependency versions

If your projects depends on a specific version of a CocoaPod, the Podfile can be used to restrict integration of the CocoaPod to that version.

*Integrate the version 0.25.0 of RestKit*  
```pod 'RestKit', '0.25.0'```

Logic operators can be used to assign minimum or maximum supported versions.

*Integrate the latest version of RestKit that is greater than 0.22.0*  
```pod 'RestKit', '>= 0.22.0'```  

Podfile supports the use of an 'optimistic operator' to allow only the last version component to increment.

*Integrate any version of RestKit from 0.2.1 up to (but not including) 0.3*  
```pod 'RestKit', '~> 0.2.1'```

If a the Pod conforms to [Semantic Versioning](https://github.com/mattbocosoft/presentation-gitflow-and-semanticversioning), using the 'optimistic operator' to allow the minor and patch version to increment, but not the major version, is a good way to ensure that the project integrates the latest version the dependency that maintains backwards compatibility.

##Installing Dependencies
Once you've added the dependencies, run the installation command on the terminal within the root directory of the project:  
```pod install```

This command will download the CocoaPod dependencies and integrate them directly into the the workspace.

##Updating Dependencies
You can update your CocoaPod dependencies following the version rules specified in the Podfile by running ```pod update```. This command will check the master CocoaPod Podspec repository, and any custom Podspec respositories you may have specified, for any updates to your dependencies, download them, and install them in your workspace.

##Uninstalling Dependencies
To remove a dependency, simply delete the associated line in the Podfile and run ```pod install``` again.


**Next Up**: [Creating a Cocoapod](creating-pods.md)  
...or return to the [homepage](README.md).
