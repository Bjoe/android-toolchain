# android-toolchain

Generate in the build folder a a conan profile/shell environment from Android cmake toolchain.

Usage:
cmake -DCMAKE_TOOLCHAIN_FILE=/PATH-TO-ANDROID-SDK/ndk-bundle/build/cmake/android.toolchain.cmake -DANDROID_NDK=/PATH-TO-ANDROID-SDK/ndk-bundle -DCMAKE_BUILD_TYPE=... -DANDROID_ABI=... -DANDROID_PLATFORM=... .../android-toolchain

Example usage for android ARMv7 API level 19 with rtti and exceptions:
cmake -DCMAKE_TOOLCHAIN_FILE=/PATH-TO-ANDROID-SDK/ndk-bundle/build/cmake/android.toolchain.cmake -DANDROID_ABI=armeabi-v7a -DANDROID_NDK=/PATH-TO-ANDROID-SDK/ndk-bundle -DCMAKE_BUILD_TYPE=Debug -DANDROID_PLATFORM=android-19 -DANDROID_CPP_FEATURES='rtti exceptions' -DANDROID_STL="c++_shared" .../android-toolchain

