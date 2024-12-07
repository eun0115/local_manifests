EvolutionX for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir evox
cd evox
```

Init the base manifest

```bash
repo init -u https://github.com/Evolution-X/manifest -b vic --git-lfs --depth=1
cd .repo 
git clone https://github.com/eun0115/local_manifests
cd ..
```

Then sync up with this command:
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j4
git clone https://github.com/Evolution-X/vendor_evolution-priv_keys-template vendor/evolution-priv/keys
cd vendor/evolution-priv/keys
./keys.sh
cd ../../..
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
riseup a71 userdebug
rise b
```
