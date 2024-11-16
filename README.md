# PenguinOS #

### Initializing Repo ###

```bash
repo init -u https://github.com/Penguin-nonsense/manifest -b unity
```

### Sync source ###

```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags --optimized-fetch --prune -j$(nproc --all)
```

## Building ##

The bundled builder tool `./rom-build.sh` handles all the building steps for the specified device automatically

```bash
./rom-build.sh <device> <flags>
```
You may include additional flags as per your requirements

• ```-t``` to set type 

```user/userdebug/eng```

• ```-s``` to specific path to your keys if you wanna use classic method of signing builds

• ```-c``` for clean build and so on...

you can check all available flags [here](https://github.com/AOSPA/android_vendor_aospa/blob/vauxite/build.sh)

 I use
 
```bash
./rom-build.sh phone1 -t user -s certs
```
