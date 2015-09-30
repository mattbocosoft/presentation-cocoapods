#Integrating Pods

By default, CocoaPods use Xcode workspaces instead of Xcode projects. So before you do anything, close the Xcode project you are working in.  

At the terminal, <code>cd</code> into the root directory of your project. You will need to create a file called **'Podfile'** (with no file-type extension). This can be done manually (<code>touch Podfile</code>) or by running the command <code>pod init</code>.  

**'Podfile'** will act as your project's CocoaPod configuration. Here you will specify your project settings and dependencies. For now we can leave this blank.

Now that you have a **'Podfile'** in place, run <code>pod install</code> at the terminal to generate the project workspace. From now on, open up the workspace file instead of the project file.

Go ahead and open up the workspace file and you should now see two sub-projects in the workspace. Expand the **Pods** workspace to reveal that the **'Podfile'** has been referenced. Click on **'Podfile'**; now we can begin adding project dependencies.
