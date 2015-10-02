#Integrating Pods

By default, CocoaPods use Xcode workspaces instead of Xcode projects. So before you do anything, close the Xcode project you are working in.  

##Create a Podfile
At the terminal, <code>cd</code> into the root directory of your project. You will need to create a file called **'Podfile'** (with no file-type extension). This can be done manually (<code>touch Podfile</code>) or by running the command <code>pod init</code>.  

The Podfile is a Ruby document which acts as your project's CocoaPod configuration. Here you will specify your project settings and dependencies.  

##Target Platform
Open the Podfile in text edit or Xcode, and begin by adding the target platform on the first line. This will be used to ensure that the dependencies are compatible.  

For a project targeting iOS, this would be:  
```platform :ios, '8.0'```

For a project targeting OS X, this woudl be:
```platform :osx, '10.11'```

If you'd like to support multiple platforms, then you might write something like this:

```
target :ios do
    platform :ios, '7.0'
    pod 'RestKit'
end

target :osx do
    platform :osx, '10.10'
    pod 'RestKit'
end
```

Next you can begin adding project dependencies.

##Project Dependencies
Once you've [found](searching-for-cocoapods.md) a CocoaPod you'd like to integrate, add it to the Podfile using its name.

*Integrate the latest version of RestKit*  
```pod 'RestKit'```  

The Podfile can have many dependencies. Each pod should be placed on its own line.

###Dependency versions

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

If you want to use the latest commit of a CocoaPod, you can use the :head flag.

```pod 'GoogleAnalytics', :head```

Here is an example of how your Podfile might look:

```
platform :ios, "7.0"

pod "AFNetworking"
pod 'NSDate+TimeAgo'
```

##Installing Dependencies
Now that you have a **'Podfile'** in place and added the project dependencies, head back to the terminal and run the installation command within the root directory of the project:  
```pod install```

This command will generate a new workspace file by default, fetch the CocoaPod dependencies' source code and integrate them directly into the the workspace. The ```pod install``` command also takes care of all project settings like linker flags, search paths, and headers.

From now on, you use the workspace file to open up your project. When you open up the workspace file in Xcode, you should now see two sub-projects in the workspace. Expand the **Pods** workspace to reveal that the **'Podfile'** has been referenced.

##Updating Dependencies
You can update your CocoaPod dependencies following the version rules specified in the Podfile by running ```pod update```. This command will check the master CocoaPod Podspec repository, and any custom Podspec respositories you may have specified, for any updates to your dependencies, download them, and install them in your workspace.

##Uninstalling Dependencies
To remove a dependency, simply delete the associated line in the Podfile and run ```pod install``` again.


**Next Up**: [Creating a Cocoapod](creating-pods.md)  
...or return to the [homepage](README.md).
