Device Trees for Samsung Galaxy A71
------------------------------------
Init the base manifest
```bash
repo init -u https://git.libremobileos.com/LMODroid/manifest.git -b fourteen --git-lfs --depth=1
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
lunch lineage_a71-ap2a-userdebug
make bacon -j$(nproc --all)
```
