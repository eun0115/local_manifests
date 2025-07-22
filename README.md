LineageOS for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir crd
cd crd
```

Init the base manifest

```bash
repo init -u https://github.com/crdroidandroid/android.git -b 15.0 --git-lfs --depth=1
git clone https://github.com/eun0115/local_manifests -b yes .repo/local_manifests 
```

Then sync up with this command:
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -v
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
lunch lineage_a71-userdebug
make bacon
```
