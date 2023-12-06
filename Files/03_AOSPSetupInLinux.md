# AOSP Setup in Linux

Hardware Requirements :

- 64-bit environment
- 250GB + 150GB disk space
- 16GB RAM minimum (64GB recommended by Google)

Software Requirements :

- Ubuntu 18.04 LTS

For detailed information, [Refer Android Docs](https://source.android.com/docs/setup/start/requirements)

## Install Required Packages

```bash
sudo apt-get install git-core gnupg flex bison build-essential zip curl zlib1g-dev libc6-dev-i386 libncurses5 x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig
```

For detailed information, [Refer Android Docs](https://source.android.com/docs/setup/start/initializing)

## Install Source Control Tool

Working with Android code requires using both Git (an open-source version-control system) and Repo (a Google-built repository-management tool that runs on top of Git).

```bash
sudo apt-get update
sudo apt-get install repo
```

For detailed information, [Refer Android Docs](https://source.android.com/docs/setup/download)

## Download the Source

### Initializing a Repo client

```bash
mkdir WORKING_DIRECTORY
cd WORKING_DIRECTORY
```

```bash
git config --global user.name Your Name
git config --global user.email you@example.com
```

```bash
repo init -u https://android.googlesource.com/platform/manifest -b BRANCH_NAME
```

### Downloading the Android source tree

```bash
repo sync
```

For detailed information, [Refer Android Docs](https://source.android.com/docs/setup/download/downloading)

## Building Android

### Setting up the environment

Initialize the environment with the `envsetup.sh` script:

```bash
. build/envsetup.sh
```

### Choosing a target

Choose which target to build with `lunch`.

```bash
lunch aosp_arm-eng
```

### Building the code

```bash
m
```

Build everything with m.

### Running the Build

You can either run your build on an emulator or flash it on a device.

Because you've already selected your build target with lunch, it's unlikely to run on a different target than it was built for.

**Flashing with fastboot**
To flash a device, use fastboot, which should be included in your path after a successful build.

**Emulating an Android device**
The emulator is added to your path automatically by the build process. To run the emulator, type:

```bash
emulator
```

For detailed information, [Refer Android Docs](https://source.android.com/docs/setup/build/building)
