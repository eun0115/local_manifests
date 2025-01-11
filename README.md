YAAP for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir yaap
cd yaap
```

Init the base manifest

```bash
repo init -u https://github.com/yaap/manifest.git -b fifteen --git-lfs --depth=1
git clone https://github.com/eun0115/local_manifests -b yaap .repo/local_manifests
```

Then sync up with this command:
```bash
repo sync -c -j4 --force-sync --no-clone-bundle --no-tags --optimized-fetch
```
-------------

Then sign with this command:
```bash
subject='/C=PH/ST=Philippines/L=Manila/O=eun0115/OU=eun0115/CN=eun0115/emailAddress=gianpaoloestacio5@gmail.com' 
for x in releasekey platform shared media networkstack verity otakey testkey sdk_sandbox bluetooth nfc; do
    ./development/tools/make_key vendor/yaap/signing/keys/$x "$subject";
done
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
lunch yaap_a71-userdebug
m yaap
```
