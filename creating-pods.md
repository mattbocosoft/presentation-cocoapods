#Creating a CocoaPod

Developers can create and distribute their own CocoaPods and distribute them in a number of ways both privately and publicly.

Each CocoaPod requires a Podspec configuration and a license file. A Podspec describes a specific version of a CocoaPod, including *"details about where the source should be fetched from, what files to use, the build settings to apply, and other general metadata such as its name, version, and description"*.

##Setting up a Podspec

You can generate a Podspec by running the following command at the terminal:

```pod spec create [Name-of-Pod]```

This command will generate a Podspec stub (Name-of-Pod.podspec) which can be filled out with the specifics of your CocoaPod.
