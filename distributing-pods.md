#CocoaPod Distribution

Depending on who your audience is, there are several different methods to distribute your Pod to other developers and projects.

##Local

If you do not need to distribute your CocoaPod because you are working with it only locally, then your Podfile can point to the local CocoaPod by simply referencing its local location:

```pod "MyPod" :path => 'LocalPods/MyPod'```

##Public

The CocoaPods [trunk](https://guides.cocoapods.org/making/getting-setup-with-trunk) is a public git repository where developers can host their Podspecs for public consumption.  


##Private

If you are part of an organization that would like to share libraries internally, then CocoaPods is great way of doing so.

1. Create a Podspec repository, and place it in a shared location where others can access it.  
2. Check to make sure it's installed correctly.  
    $ cd [PODSPEC_DIRECTORY]
    $ pod repo lint .
3. Add your Podspec to your private Podspec repository  
    $ pod repo push [REPO_NAME] [SPEC_NAME].podspec

In order for CocoaPods to find your private Pods, you need to tell it where your Podspec repository is located. If you want all your projects to be aware of your private repository, then you can add your private Podspec repository to your CocoaPods installation:  

```pod repo add REPO_NAME SOURCE_URL```

Or if you are only using the private repository for a single project, then you canadd your private Podspec repository as a source in your project's Podfile:  

```source 'SOURCE_URL'```

For more information about private Podspec repositories, check out [https://guides.cocoapods.org/making/private-cocoapods](https://guides.cocoapods.org/making/private-cocoapods)

**Previous**: [CocoaPod Distribution](distributing-pods.md)  
**Next Up**: [Further reading](Further-reading-and-resources.md)
...or return to the [homepage](README.md).
