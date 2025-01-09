RisingOS for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir rising
cd rising
```

Init the base manifest
```bash
repo init -u https://github.com/RisingTechOSS/android -b fifteen --git-lfs --depth=1
cd .repo 
git clone https://github.com/eun0115/local_manifests 
cd ..
```

Then sync up with this command:
```bash
repo sync -c -j66 --force-sync --no-clone-bundle --no-tags --optimized-fetch
```

Pick rising bringup
```bash
cd device/samsung/a71
git fetch https://github.com/RisingTechOSS-devices/device_samsung_a71
git cherry-pick 78a9db56a4bfa15b851b735d241234f559500a53 d63c6b7a485fe74f0cfb36e323b74bed95a401ca
cd ../../..
```

_Building from source_
---------------
```bash
. build/envsetup.sh
riseup a71 userdebug
gk -s
rise b
```
