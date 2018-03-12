# android-toolchain

Generate in the build folder a a conan profile/shell environment from Android cmake toolchain.

Usage:
/PATH-TO-ANDROID-SDK/cmake/..../bin/cmake -DCMAKE_TOOLCHAIN_FILE=/PATH-TO-ANDROID-SDK/ndk-bundle/build/cmake/android.toolchain.cmake -DANDROID_NDK=/PATH-TO-ANDROID-SDK/ndk-bundle -DANDROID_ABI=... -DANDROID_PLATFORM=... .../android-toolchain

For ANDROID_ABI and ANDROID_PLATFORM see https://developer.android.com/ndk/guides/cmake.html

Example usage for android ARMv7 API level 19 with rtti and exceptions:
/PATH-TO-ANDROID-SDK/cmake/..../bin/cmake -DCMAKE_TOOLCHAIN_FILE=/PATH-TO-ANDROID-SDK/ndk-bundle/build/cmake/android.toolchain.cmake -DANDROID_NDK=/PATH-TO-ANDROID-SDK/ndk-bundle -DCMAKE_MAKE_PROGRAM=PATH-TO-ANDROID-SDK/cmake/..../bin/ninja -DCMAKE_BUILD_TYPE=Debug -DANDROID_ABI=armeabi-v7a -DANDROID_PLATFORM=android-19 -DANDROID_CPP_FEATURES='rtti exceptions' -DANDROID_STL="c++_shared" .../android-toolchain

