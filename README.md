# AOSP
# Sync

# Initialize local repository
repo init -u git://github.com/FurySnailx/android-1.git -b pie

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
# Build
# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -jX
