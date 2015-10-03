#CocoaPod Distribution

Depending on who your audience is, there are several different methods to distribute your Pod to other developers and projects.

The CocoaPods [trunk](https://guides.cocoapods.org/making/getting-setup-with-trunk) is a public git repository where developers can host their Podspecs for public consumption.  

##Local

If you are working on a Pod locally, then you don't need to have the Podspec anywhere but the root directory of the Pod. Then in the demo project, simply reference the local location of the Pod like this:

```pod "MyPod" :path => 'LocalPods/MyPod'```

##Public

##Private

**Previous**: [CocoaPod Distribution](distributing-pods.md)  
**Next Up**: [Further reading](Further-reading-and-resources.md)
...or return to the [homepage](README.md).
