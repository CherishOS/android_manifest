### android_manifest
1. Run the following commands to initialize the repo 
```bash
    repo init -u https://github.com/CherishOS/android_manifest.git -b twelve 
```
&nbsp; &nbsp; &nbsp; Or to save more time and space, you can do a shallow clone using
```bash
    repo init -u https://github.com/CherishOS/android_manifest.git --depth=1 -b twelve 
```
2. Then try to sync up the source 

```bash
    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

3. Once the source is synced, prepare your device trees, dependencies and start the build by the following commands

```
   . build/envsetup.sh
   ccache -M 100G # to boost up build time
   brunch cherish_<devicecodename>-<varient>
```

4. To make gapps build add following in cherish_device.mk
```
WITH_GMS := true 
```
