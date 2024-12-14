# Expo Image Component - Android Local Image Loading Issue with Special Characters

This repository demonstrates a bug in the Expo `Image` component on Android where local images with special characters in their URIs fail to load. The issue is specific to Android; iOS functions correctly. 

## Bug Description

The `Image` component correctly displays images when using URIs without special characters (e.g., spaces, accented characters). However, when special characters are present, the image fails to load without throwing an error. The file exists, and the URI is correctly formatted.  This makes debugging difficult.

## Steps to Reproduce

1. Clone the repository.
2. Run the project on an Android emulator or device.
3. Observe that the image with special characters in its URI does not load.
4. Run the project on an iOS simulator or device; the image should load correctly.

## Solution

The solution involves URL encoding the URI before passing it to the `Image` component.  This ensures that special characters are properly handled by the Android system.