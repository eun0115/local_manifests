BlissROM for Samsung Galaxy A71
------------------------------------

Create directories
```bash
mkdir bliss
cd bliss
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
for apex in com.android.adbd com.android.adservices com.android.adservices.api com.android.appsearch com.android.appsearch.apk com.android.art com.android.bluetooth com.android.btservices com.android.cellbroadcast com.android.compos com.android.configinfrastructure com.android.connectivity.resources com.android.conscrypt com.android.devicelock com.android.extservices com.android.graphics.pdf com.android.hardware.authsecret com.android.hardware.biometrics.face.virtual com.android.hardware.biometrics.fingerprint.virtual com.android.hardware.boot com.android.hardware.cas com.android.hardware.neuralnetworks com.android.hardware.rebootescrow com.android.hardware.wifi com.android.healthfitness com.android.hotspot2.osulogin com.android.i18n com.android.ipsec com.android.media com.android.media.swcodec com.android.mediaprovider com.android.nearby.halfsheet com.android.networkstack.tethering com.android.neuralnetworks com.android.nfcservices com.android.ondevicepersonalization com.android.os.statsd com.android.permission com.android.profiling com.android.resolv com.android.rkpd com.android.runtime com.android.safetycenter.resources com.android.scheduling com.android.sdkext com.android.support.apexer com.android.telephony com.android.telephonymodules com.android.tethering com.android.tzdata com.android.uwb com.android.uwb.resources com.android.virt com.android.vndk.current com.android.vndk.current.on_vendor com.android.wifi com.android.wifi.dialog com.android.wifi.resources com.google.pixel.camera.hal com.google.pixel.vibrator.hal com.qorvo.uwb; do \
subject='/C=PH/ST=Philippines/L=Manila/O=eun0115/OU=eun0115/CN=eun0115/emailAddress=gianpaoloestacio5@gmail.com'  \
    ~/.android-certs/make_key ~/.android-certs/$apex "$subject"; \
    openssl pkcs8 -in ~/.android-certs/$apex.pk8 -inform DER -out ~/.android-certs/$apex.pem; \
done
```
-------------

_Building from source_
---------------
```bash
. build/envsetup.sh
blissify -g a71
```
