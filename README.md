# Create your own NikGapps build [BETA]
Repository to upload config file for NikGapps Nightly Cycle to create a custom build for you

## Prerequisite
- Working knowledge of NikGapps configuration file
- That's it. No server, No core Gapps knowledge, No other cost!

## How it'll work?
- Fork [this repository](https://github.com/nikgapps/config) (Find the fork icon on top right corner of this page)

![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkRepo.png)

- Wait till the forking is finished

![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkingRepo.png)

- Once finished, Download the latest version of [nikgapps.config](https://sourceforge.net/projects/nikgapps/files/Releases/Config/nikgapps-config/) (Always)
- Copy the file to specific target android version folder (for e.g, config must be part of '10' folder if you wish to create a build targeting android 10, similarly for android 11)
- Configure your config file, set the `AppSet=1` or `>>Package=1` which you want to keep in your package. For e.g. YouTube=1, PixelLauncher=1, >>PixelTips=1 (any other values will be ignored)
- Rename the config file and set the name you want to give your custom NikGapps build to. For e.g. xyz.config will create NikGapps-xyz-arm64-androidversion-date-signed.zip 
- Commit the config file to your forked repository (make sure the name is unique, it can be anything with extention '.config')
- Send a pull request to merge your config file in this repository
- Wait for the pull request to get merged
- Once the pull request is merged, NikGapps nightly cycle will build your desired gapps
- Once your custom gapps package is build, the config file will be moved to archive with '_date' appended to it
- Find the date folder in [Config-Releases](https://sourceforge.net/projects/nikgapps/files/Config-Releases/) where you will find your build created

## How to request for a custom build again
- Follow above steps again as once the custom build is created, config file will be moved to archive

