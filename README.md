# AOSP
Sync
# Initialize local repository
repo init -u https://github.com/FurySnailx/manifest -b ten

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
Build
# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -jX
