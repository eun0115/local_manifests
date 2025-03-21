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
git clone https://github.com/eun0115/local_manifests -b main
cd ..
```

Then sync up with this command:
```bash
repo sync -j$(nproc --all) --no-tags --no-clone-bundle --current-branch
```
-------------

Then sign with this command:
```bash
git clone https://github.com/Evolution-X/vendor_evolution-priv_keys-template vendor/evolution-priv/keys ; cd vendor/evolution-priv/keys ; ./keys.sh ; cd ../../..
```
-------------



_Building from source_
---------------
```bash
. build/envsetup.sh
riseup a71 userdebug
rise b
```
