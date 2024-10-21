RisingOS for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir rising
cd rising
```

Init the base manifest

```bash
repo init -u https://github.com/RisingTechOSS/android -b fourteen --git-lfs --depth=1
```
  
Add the local manifest

  Take the xml file for your device and copy it to .repo/local_manifests/

Then sync up with this command:
```bash
repo sync -c --no-clone-bundle --optimized-fetch --prune --force-sync -j$(nproc --all)
```
-------------
 
_Building from source_
---------------
```bash
riseup a71 userdebug
```
