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
cd .repo 
git clone https://github.com/eun0115/local_manifest
cd ..
```

Then sync up with this command:
```bash
repo sync -j$(nproc --all) --no-tags --no-clone-bundle --current-branch 
```
-------------
 
_Building from source_
---------------
```bash
riseup a71 userdebug
```
