YAAP for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir pos
cd pos
```

Init the base manifest

```bash
repo init -u https://github.com/BlissRoms/stable_releases.git -b refs/tags/v18.3-stable-voyager --git-lfs --depth=1
git clone https://github.com/eun0115/local_manifests -b fifteen .repo/local_manifests
```

Then sync up with this command:
```bash
repo sync -j$(nproc --all) --no-tags --no-clone-bundle --current-branch
```
-------------

Then sign with this command:
```bash
wget https://raw.githubusercontent.com/306bobby-android/crDroid-build-signed-script/main/create-signed-env.sh ; chmod +x create-signed-env.sh ; ./create-signed-env.sh
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
blissify -g a71
```
