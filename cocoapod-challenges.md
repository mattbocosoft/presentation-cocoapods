#Pain Points and their Remedies

It's important to also be aware of what you are losing as a developer by using CocoaPods instead of its alternatives. In my experience, the biggest drawback of CocoaPods as a consumer is the loss of control over dependency content. Of course if the CocoaPod in question only serves to wrap a black-box library (*.a) instead of an open-source library, then the consumer never had this control in the first place.

There are two pain points that I have experienced with using CocoaPods:  
1. Modifying library code  
2. Gaining access to Pod history  

Luckily however, there is a rememdy for both of these issues.

####Modifying Pod Content within Context
If you find a bug in a dependency, then it requires a bit of work to access and modify the code.

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
