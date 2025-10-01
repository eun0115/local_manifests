LineageOS for Samsung Galaxy M20
------------------------------------

Create directories
```bash
mkdir los
cd los
```

Init the base manifest

```bash
repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs --depth=1
git clone https://github.com/eun0115/local_manifests -b wisdom .repo/local_manifests
```

Then sync up with this command:
```bash
repo sync -c -v --force-sync --no-clone-bundle --no-tags --optimized-fetch
```
-------------

Then sign with this command:
```bash
https://github.com/306bobby-android/crDroid-build-signed-script
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
lunch lineage_wisdom-userdebug
make bacon
```
