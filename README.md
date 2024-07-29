# Create your own NikGapps build in less than 30 minutes
Repository to upload config file for NikGapps ecosystem to create a custom build for you  


## Builds Created So Far

[![Downloads](https://img.shields.io/badge/dynamic/json?color=blueviolet&label=Total%20Created%20&query=total&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=brightgreen&label=Android%2014.0%20&query=U&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=blue&label=Android%2013.0%20&query=T&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=brown&label=Android%2012.1%20&query=SL&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=yellowgreen&label=Android%2012.0%20&query=S&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=red&label=Android%2011.0%20&query=R&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)  
[![Downloads](https://img.shields.io/badge/dynamic/json?color=green&label=Android%2010.0%20&query=Q&url=https%3A%2F%2Fraw.githubusercontent.com%2Fnikgapps%2Ftracker%2Fmain%2Fcount.json&cacheSeconds=900)](https://raw.githubusercontent.com/nikgapps/tracker/main/count.json)

## Prerequisite
- Working knowledge of [NikGapps configuration file](https://nikgapps.com/misc/2022/02/22/NikGapps-Config.html)
- That's it. No server, No core Gapps knowledge, No other cost!

## Is there a video tutorial to create a custom build?
- Yes, if you want to skip reading and jump to video tutorial. Here is the [video tutorial](https://youtu.be/jZWR9Wz7hMk) that you should follow to create a custom build.

## How it works

1. **Fork this repository**: Click on the fork icon at the top right corner of the [repository page](https://github.com/nikgapps/config).

   ![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkRepo.png)

2. **Wait for the forking to finish**.

   ![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/ForkingRepo.png)

3. **Download the latest version of the [nikgapps.config](https://sourceforge.net/projects/nikgapps/files/NikGappsConfigs/)**.
4. **Copy the downloaded file** to the specific target Android version folder (e.g., place the config file in the '10' folder if you want to create a build targeting Android 10).

   **Note:** Do not reuse, modify, or delete any existing '.config' files from any of the folders to avoid issues during building and troubleshooting.
5. **Rename the config file**: Set the name you want for your custom NikGapps build. For example, renaming to `xyz.config` will create `NikGapps-xyz-arm64-androidversion-date-signed.zip`.
6. **Configure your config file**: Set `AppSet=1` or `>>Package=1` to include it in your package, or set it to `0` to exclude it.
   - You can also set packages to `2` to include them in your package and prevent the AOSP package from being removed when your package is installed.
   - Example: `YouTube=1`, `PixelLauncher=1`, `>>PixelTips=1` will include these packages in your custom Gapps build, while `Drive=0` will skip the package. Any other values will be ignored.
7. **Commit the config file** to your forked repository. Ensure the name is unique and ends with '.config'.
8. **Send a pull request** to merge your config file into this repository.
9. **Wait for the pull request to be merged**: This should take less than 30 minutes.
10. **Once merged**, the NikGapps ecosystem will build your custom Gapps.
11. **After the build**, your config file will be moved to the archive with '_date' appended to it.
12. **Find your build**: Look for the date folder in [Config-Releases](https://sourceforge.net/projects/nikgapps/files/Config-Releases/), where you will find your build.

## How to request for a custom build again
- Follow above steps again as once the custom build is created, config file will be moved to archive

## Blog

For More information on [this repository](https://github.com/nikgapps/config), refer [nikgapps blog](https://nikgapps.com/misc/2021/04/10/Build-Own-NikGapps-Build.html)

