EvoX for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir evox
cd evox
```

Init the base manifest

```bash
repo init -u https://github.com/Evolution-X/manifest -b udc --git-lfs --depth=1
cd .repo 
git clone https://github.com/eun0115/local_manifests
cd ..
```

Then sync up with this command:
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j4
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
riseup a71 userdebug
rise b
```
