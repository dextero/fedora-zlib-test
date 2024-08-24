# zlib test

```
# builds fine on Fedora (OFF is CMake's default btw)
cmake -DCMAKE_FIND_PACKAGE_PREFER_CONFIG=OFF -H. -Bbuild

# changing CMAKE_FIND_PACKAGE_PREFER_CONFIG requires a clean rebuild
rm -rf build

# looks for zlib using /usr/lib64/cmake/ZLIB/ZLIB.cmake rather than
# /usr/share/cmake/Modules/FindZLIB.cmake and fails
cmake -DCMAKE_FIND_PACKAGE_PREFER_CONFIG=ON -H. -Bbuild
```

See https://cmake.org/cmake/help/latest/variable/CMAKE_FIND_PACKAGE_PREFER_CONFIG.html
