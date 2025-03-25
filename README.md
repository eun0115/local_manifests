LineageOS for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir rising
cd rising
```

Init the base manifest

```bash
repo init -u https://github.com/RisingOS-Revived/android -b fifteen --git-lfs --depth=1
git clone https://github.com/eun0115/local_manifests -b rising-fifteen-qpr2 .repo/local_manifests
```

Then sync up with this command:
```bash
repo sync -j8 --no-tags --no-clone-bundle --current-branch
```
-------------

Then sign with this command:
```bash
gk -s
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
riseup a71 userdebug
rise sb
```
