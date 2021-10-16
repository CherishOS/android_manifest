# android_manifest
```bash
    repo init -u https://github.com/CherishOS/android_manifest.git -b twelve 
```

Then to sync up:
================

```bash
    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
