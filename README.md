Getting Started
-

### Requirements:
- You have basic knowledge of [Repo](https://source.android.com/source/using-repo.html) and Version Control with [Git](https://source.android.com/source/version-control.html).
- Make sure you have an [Android Build Environment](https://source.android.com/setup/build/initializing) and the [Repo Tool](https://source.android.com/setup/build/downloading) set up.
- 100GB of disk space (500GB recommended).

Compiling SkyzenOS
-

### First you need to initialize your local repository using the following command:
```
repo init -u https://github.com/SkyzenOS/manifest.git -b skyzen-16 --git-lfs
```
### Then Sync the source code using the following command:
```
repo sync -j$(nproc --all) --force-sync --no-tags --no-clone-bundle --prune --optimized-fetch
```
### Now adapt your Device Tree for SkyzenOS and start the build using the following commands:
```
. build/envsetup.sh
lunch skyzen_$device-bp4a-userdebug
mka skyzen
```

Build flags
-

Skyzen maintainer:
```makefile
SKYZEN_MAINTAINER := Kultrinhaa_
```

Now fix the errors during compilation and wait for successful build message.

### Happy Compiling!

Credits
-

- [GenesisOS](https://github.com/GenesisOS)

Thanks to the whole custom ROM Community.
