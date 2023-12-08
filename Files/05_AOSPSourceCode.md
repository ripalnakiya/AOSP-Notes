# AOSP Source Code

## art

ART (Android Runtime) operating environment is located in the `art/` directory.

It also includes dex complier, JVM, JIT, Dalvik VM etc.

## bionic

This directory contains the **C library** (libc) used by Android.

It includes low-level system components like the standard C library, **dynamic linker**, and other essential **runtime components**.

## bootable

This directory contains the **bootloader** (which is responsible for **loading the Android kernel** and **initiating the system boot process**), recovery image, and other low-level system software that is typically loaded before the kernel.

## build

Directory contains the **build system** for Android.

It includes **tools and scripts** for **building** the entire Android system, **managing dependencies**, and **generating the final system images**.

Contains :

- `envsetup.sh` script that initializes the build environment.
- `Android.mk` file that defines the build rules for the entire Android system.
- make and soong build systems.

## cts

Contains the Compatibility Test Suite (CTS) for Android.

CTS is used to **check for incompatibilities** with Android OS **during device development**.

## dalvik

It contains the Dalvik Virtual Machine related code.

Even though ART is the default runtime environment for Android, android still uses Dalvik VM for **running apps that are not compiled with ART**.

It also contains **dex code generator**, and Dalvik exchange.

## developers

Contains demo and **sample android projects**.

## development

It includes **tools** for debugging, profiling, and testing Android applications.

## device

It contains **device specific files and configurations**.

It includes supporting configuration and driver files required for Development boards like linaro, hikey etc.

## external

Includes **external projects and libraries** that Android uses but are not part of the core AOSP.

These could be **open-source projects** or third-party libraries.

For example, **Dagger2**

## frameworks

Contains the **core Android system framework**.

We can find all the **System service**(`ActivityManagerService.java`, `PackageManagerService.java`), **libraries**, and **APIs** that are used by the Android system.

## hardware

Contains the hardware abstraction layer (HAL) for Android.

It consists of HAL for audio, video, TV, camera, USB, and other hardware components.

Contains **hardware-specific code**, including drivers for various hardware components like sensors, cameras, and audio devices.

## kernel

It contains the **kernel configuration** and **prebuilts**.

## libcore

The `/libcore` directory includes **core libraries used by the Android system**.

These libraries provide **fundamental functionality for Java** applications on Android, such as **I/O operations**, utilities, and **networking**.

## libnativehelper

This directory contains **helper code for native development** .

It provides support for integrating native (C/C++) code with the Java-based Android framework.

## out

**After the build is complete**, the output is placed in the `/out` directory.

The `/out` directory is where the build system places the output artifacts, including compiled binaries, libraries, and **system images**.

## packages

The `/packages` directory includes various **Android applications and system packages**.

It contains source code for apps like the Android Browser, Calculator, Calendar, and others.

## pdk

The Platform Development Kit (PDK) includes **tools and documentation for building Android devices**.

It provides **resources for device manufacturers** to create Android-compatible hardware.

It includes only necessary components for developing HAL.

## platform_testing

Consists of **platform tests modules**.

## prebuilts

The `/prebuilts` directory contains prebuilt binaries and tools that are used in the Android build process.

It includes toolchains like **asuite**, **android emulator**, bazel etc.

## sdk

It contains **instructions and tools for building the Android SDK**, for a specific build.

## system

It contains **low level file system libraries**, applications and components.

Folders for **SELinux**, Logging and many low level configuration files.

## test

It contains **test suits** like csuite, vts(vendor test suite), mts(mainline test suite) etc.

## toolchain

It contains **files related to benchmark** and **pgoprofiles**.

## tools

It contains **tools like apksig, asuite, trade federation** etc.
