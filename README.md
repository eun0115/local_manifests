RisingOS for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir rising
cd rising
```

Init the base manifest

```bash
repo init -u https://github.com/RisingOS-staging/android -b fifteen --git-lfs --depth=1
cd .repo 
git clone https://github.com/eun0115/local_manifests
cd ..
```

Then sync up with this command:
```bash
repo sync -c -j66 --force-sync --no-clone-bundle --no-tags --optimized-fetch
```
-------------

Then sign with this command:
```bash
. build/envsetup.sh
riseup a71 userdebug
gk -s
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
riseup a71 userdebug
rise b
```
