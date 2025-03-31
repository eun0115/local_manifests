LineageOS for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir los
cd los
```

Init the base manifest

```bash
repo init -u https://github.com/LineageOS/android.git -b lineage-22.2 --git-lfs --depth=1
git clone https://github.com/eun0115/local_manifests -b fifteen .repo/local_manifests
```

Then sync up with this command:
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
lunch lineage_a71-userdebug
make bacon
```
