Getting Started
-
### Requirements:
- A Linux build environment with the [AOSP dependencies](https://source.android.com/docs/setup/build/initializing) installed.
- Git, [Repo](https://source.android.com/docs/setup/develop/repo), and Git LFS configured.
- At least 250 GB of free disk space (400 GB recommended).

Compiling SkyzenOS
-

### Initialize the repository:
```bash
repo init -u https://github.com/SkyzenOS/manifest.git -b skyzen-16 --git-lfs
```

### Sync the source code:
```bash
repo sync
```

### Build:
Before building, make sure your device tree is adapted for SkyzenOS and defines a product named `skyzen_<codename>`.

```bash
source build/envsetup.sh
brunch <codename>
```

The same build can be started manually with:

```bash
source build/envsetup.sh
lunch skyzen_<codename>-bp2a-userdebug
mka skyzen
```

Now fix the errors during compilation and wait for successful build message.

### Happy Compiling!

Credits
-
- [LineageOS](https://github.com/LineageOS)
- [GenesisOS](https://github.com/GenesisOS)
