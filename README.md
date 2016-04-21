Local manifests to build CyanogenMod 12.1 for Xiaomi Mi2.

How to build:
-------------

Initialize repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-12.1
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/akorshun/android_local_manifests/cm-12.1/local_manifest.xml
    curl --create-dirs -L -o .repo/local_manifests/remove.xml -O -L https://raw.githubusercontent.com/akorshun/android_local_manifests/cm-12.1/remove.xml
    repo sync

Compile:

    . build/envsetup.sh
    lunch cm_aries-userdebug
    mka otapackage
