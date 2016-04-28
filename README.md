Local manifests to build BlissPop 4.0.3 (Android 5.1.1) for Xiaomi Mi2.

How to build:
-------------

Initialize repo:

    repo init -u https://github.com/TeamBliss-LP/android.git -b lp5.1
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/akorshun/android_local_manifests/lp5.1/local_manifest.xml
    repo sync

Compile:

    . build/envsetup.sh
    lunch bliss_aries-userdebug
    mka otapackage
