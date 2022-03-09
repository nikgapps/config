# Create your own NikGapps build in less than 30 minutes
Repository to upload config file for NikGapps ecosystem to create a custom build for you  


[![Downloads](https://img.shields.io/badge/dynamic/json?color=green&label=Android%2012%20Builds%20Created%20So%20Far&query=12&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=red&label=Android%2011%20Builds%20Created%20So%20Far&query=11&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=blue&label=Android%2010%20Builds%20Created%20So%20Far&query=10&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)

## Prerequisite
- Working knowledge of [NikGapps configuration file](https://nikgapps.com/misc/2020/11/22/NikGapps-Config.html)
- That's it. No server, No core Gapps knowledge, No other cost!

## Is there a video tutorial to create a custom build?
- Yes, if you want to skip reading and jump to video tutorial. Here is the [video tutorial](https://youtu.be/jZWR9Wz7hMk) that you should follow to create a custom build.

## How it'll work?
- Fork [this repository](https://github.com/nikgapps/config) (Find the fork icon on top right corner of this page)

![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkRepo.png)

- Wait till the forking is finished

![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkingRepo.png)

- Once finished, Download the latest version of [nikgapps.config](https://sourceforge.net/projects/nikgapps/files/Releases/Config/nikgapps-config/) (Always)
- Copy the downloaded file to specific target android version folder (for e.g, config must be part of '10' folder if you wish to create a build targeting android 10, similarly for android 11)  
**<ins>NOTE:</ins>** Do not reuse/modify or delete any existing '.config' files from any of the folders to avoid problems during building and troubleshooting 
- Rename the config file you downloaded and set the name you want to give your custom NikGapps build to. For e.g. `xyz.config` will create `NikGapps-xyz-arm64-androidversion-date-signed.zip` 
- Configure your config file, set `AppSet=1` or `>>Package=1` if you want to keep it in your package, else set it to `0`  
For e.g. `YouTube=1`, `PixelLauncher=1`, `>>PixelTips=1` will keep these packages in your custom gapps build while `Drive=0` will skip the package (Any other values will be ignored)  
- Commit the config file to your forked repository (make sure the name is unique, it can be anything with extention '.config')
- Send a pull request to merge your config file in this repository
- Wait for the pull request to get merged (should take less than 30 mins)
- Once the pull request is merged, NikGapps ecosystem will build your desired gapps
- Once your custom gapps package is build, the config file will be moved to archive with '_date' appended to it
- Find the date folder in [Config-Releases](https://sourceforge.net/projects/nikgapps/files/Config-Releases/) where you will find your build created

## How to request for a custom build again
- Follow above steps again as once the custom build is created, config file will be moved to archive

## Self make your custom build 
### Prerequisites
Make sure you have [python3](https://www.python.org/), [git](https://git-scm.com/), [aapt](https://packages.debian.org/buster/aapt) installed.
```
python3 -m pip install wheel setuptools testresources
```
### Building
- Git clone [the build scripts](https://github.com/nikgapps/build) Into a directory:
```
git clone https://github.com/nikgapps/build.git --depth=1
```
- Install needed dependencies for building:
```
cd build
pip3 install -r requirements.txt
cd ..
```
- Set GIT_CHECK and BUILD_CONFIG to False in Config.py inside build scripts directory using your Editor
  - (Optional) Set SIGN_ZIP to False to disable signing
```
<EDITOR> build/Config.py
```
- Git clone [this repository](https://github.com/nikgapps/config) Into a directory:
  - NOTE: this must be placed in the same root directory as the build scripts.
```
git clone https://github.com/nikgapps/config.git --depth=1
```
- Download the latest version of [nikgapps.config](https://sourceforge.net/projects/nikgapps/files/Releases/Config/nikgapps-config/) and place it inside your desired android version you will be building e.g. `<config dir>/<android ver>/nikgapps.config` and edit it to your liking.
- Rename the config file you downloaded and set the name you want to give your custom NikGapps build to. e.g. `xyz.config` will create `NikGapps-xyz-arm64-androidversion-date-signed.zip` 
- Finally, Build.
```
cd build
python3 config_control.py <android ver>
```
You should now have a custom NikGapps with your own Configuration.

## Blog

For More information on [this repository](https://github.com/nikgapps/config), refer [nikgapps blog](https://nikgapps.com/misc/2021/04/10/Build-Own-NikGapps-Build.html)

