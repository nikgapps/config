# Create your own NikGapps build
Repository to upload config file for NikGapps build to create a custom package

## How it'll work?
- Fork [this repository](https://github.com/nikgapps/config)

![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkRepo.png)

- Wait till the forking is finished

![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkingRepo.png)

- Once finished, configure your [nikgapps.config](https://sourceforge.net/projects/nikgapps/files/Releases/Config/nikgapps-config/) (download the latest version always)
- Set the AppSet=1 or >>Package=1 which you want to keep in your package. For e.g. YouTube=1, PixelLauncher=1, >>PixelTips=1 (any other values will be ignored)
- Rename the config file and set the name you want to give your custom NikGapps build to. For e.g. xyz.config will create NikGapps-xyz-arm64-androidversion-date-signed.zip 
- Commit the config file to your forked repository (make sure the name is unique, it can be anything with extention config)
- Send a pull request to merge your config file in this repository
- Wait for the NikGapps nightly cycle to build your desired gapps

## How to request for a custom build
- Follow above steps as once the custom build is created, config file will be moved to archive

