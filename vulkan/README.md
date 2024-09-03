# Vulkan
Vulkan dumps the main PE image of a process from memory to your disk. It targets processes protected by dynamic code encryption, implemented by the [hyperion](https://roblox.fandom.com/wiki/Hyperion) and [theia](https://reversingthread.info/index.php/2024/01/10/the-finals-defeating-theia-packer/) anti-tamper solutions. Vulkan constantly queries pages in the `.text` section of the target process and caches pages of code as they decrypt themselves. After a desired amount of the application has been decrypted (configurable via `--decrypt`) the restored PE image is saved to the disk, ready for analysis.

Vulkan has been test on [Roblox](https://roblox.com) and [The Finals](https://www.reachthefinals.com/).

## How to use
After downloading the latest version from the [releases](https://github.com/atrexus/vulkan/releases) tab, you can run it from the command line like so:
```
vulkan.exe -p <TARGET_PROCESS> -o <OUTPUT_DIRECTORY>
```

## Contributing
If you have anything to contribute to this project feel free to send a pull request and I will review it. If you want to contribute but are not sure what, check out the [issues](https://github.com/atrexus/vulkan/issues) tab for the latest stuff I need help with.
