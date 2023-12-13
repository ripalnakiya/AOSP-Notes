# Android Overlays

Resource overlay refers to the **ability to customize or extend resources**, such as layouts, drawables, or strings, **without modifying the original source code** or resources of an Android application.

A runtime resource overlay (RRO) is a package that **changes the resource values** of a target **package at runtime**.

It overlays the resources of the system with the resources of the app, **during the runtime** of the app.

In simple terms, it is a APK with only Resources.

> This concept is particularly useful for **creating variations of an app** for different devices or regions without duplicating the entire codebase.

## Static Overlays

Static overlays are enabled at build time, and cannot be disabled later.

In order to change the static overlay, you need to rebuild the ROM.

## Dynamic Overlays

Dynamic overlays are enabled at runtime, and can be enabled or disabled later, programatically.
