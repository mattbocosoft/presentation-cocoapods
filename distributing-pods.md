#CocoaPod Distribution

Depending on who your audience is, there are several different methods to distribute your Pod to other developers and projects.

##Getting ready for distribution

There are a few steps to take before starting to distribute your Cocoapod.

####Tag your Repo

Make sure to version your library by tagging the appropriate commits with version numbers so that consumers can reference exactly which version of the library that they would like to use.  

####Check for Errors

Before distributing your Pod, you need to check to make sure it doesn't have any errors. Indeed this step is mandatory if you are pushing to the public Pod trunk. There are two ways of doing this:

```$ pod spec lint```  
  This command accesses the network to check the external repo and associated tag.  

```$ pod lib lint```  
  This command accesses does not access the network in order to check for errors.  

##Distribute as an independent CocoaPod

If you do not wish to distribute your CocoaPod to a wide audience via a Podspec repository, you can use it as a standalone CocoaPod either locally or remotely.


####Local
In your project's Podfile, point to the local CocoaPod by simply referencing its local location:

```pod "MyPod" :path => 'LocalPods/MyPod'```

####Remote

```pod '[PODNAME]', :git => 'https://github.com/[USERNAME]/[PODNAME].git'```

##Distribute via a Podspec Repository

Each version of a CocoaPod must have it's own Podspec. The Podspec repository hosting the Podspec will look follow this structure:  

```
[PODSPEC_REPO]  
└── [POD_NAME]  
        └── [VERSION]  
                └── [POD_NAME].podspec  
        └── [VERSION]  
                └── [POD_NAME].podspec  
```

####Public

The CocoaPods [trunk](https://guides.cocoapods.org/making/getting-setup-with-trunk) is a public git repository where developers can host their Podspecs for public consumption.  

In order to push Pods to the trunk, developers must first sign-up with an account by registering a per-computer session-token with trunk.

```$ pod trunk register name@address.com '[YOUR_NAME]' --description='Give your session some context'```

When the library and Pod specification file is ready to be published, run lint on your pod according to the first section above to make sure its configured properly. Remember that you cannot publish your pod if lint returns any warnings or errors. If you received none, then you can go ahead and deploy your pod to the public trunk:

```$ pod trunk push [NAME.podspec]```

Deploying will kick off a notification to online CocoaPod feeds to alert other users of the new Pod. E.g. CocoaDocs.org, @CocoaPodsFeed and [CocoaPods RSS Feed](https://feeds.cocoapods.org).

For more information about distributing via the public trunk, see [https://guides.cocoapods.org/making/getting-setup-with-trunk](https://guides.cocoapods.org/making/getting-setup-with-trunk).

####Private

If you are part of an organization that would like to share libraries internally, then CocoaPods is great way of doing so.

1. Create a Podspec repository, and place it in a shared location where others can access it.  
2. Check to make sure it's installed correctly.  
```    $ cd [PODSPEC_DIRECTORY]```
```    $ pod repo lint .```
3. Add your Podspec to your private Podspec repository  
```    $ pod repo push [REPO_NAME] [SPEC_NAME].podspec```

In order for CocoaPods to find your private Pods, you need to tell it where your Podspec repository is located. If you want all your projects to be aware of your private repository, then you can add your private Podspec repository to your CocoaPods installation:  

```pod repo add REPO_NAME SOURCE_URL```

Or if you are only using the private repository for a single project, then you canadd your private Podspec repository as a source in your project's Podfile:  

```source 'SOURCE_URL'```

For more information about private Podspec repositories, check out [https://guides.cocoapods.org/making/private-cocoapods](https://guides.cocoapods.org/making/private-cocoapods)

**Previous**: [Creating a Cocoapod](creating-pods.md)  
**Next Up**: [Further reading](Further-reading-and-resources.md)  
...or return to the [homepage](README.md).
