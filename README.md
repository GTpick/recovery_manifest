#Setting up a minimal tree for building TWRP
##Android 5.1 branch
This repo is ~2.6GB
###To initialize the main repository:

````
repo init -u https://github.com/ast261/recovery_manifest.git -b android-5.1
````
Then add anyrecovery/device trees/kernels you need to a file (one XML for each device) and add them to the .repo/local_manifests folder of your initialized repo folder.

Once added:
````
repo sync
````
Done

To build recovery:
````
. build/envsetup.sh
lunch (devicename)
make installclean
time make recoveryimage
````


Devices tested:

````
Motorola Moto G 2014 (titan)
````
