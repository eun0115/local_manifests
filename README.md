YAAP for Samsung Galaxy A71
------------------------------------

Create directories

	$ mkdir yaap
	$ cd yaap

Init the base manifest

	$ repo init -u https://github.com/yaap/manifest.git -b fourteen --git-lfs
  
Add the local manifest

  Take the xml file for your device and copy it to .repo/local_manifests/

Then sync up with this command:

	$ repo sync -j$(nproc --all) --no-tags --no-clone-bundle --current-branch 

-------------
 
_Building from source_
---------------

	$ . build/envsetup.sh
	$ lunch yaap_a71-ap2a-userdebug
	$ m yaap