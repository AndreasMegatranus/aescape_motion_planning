# aescape_utils_cpp
Common code and utilities used across the Aescape C++ stack.

## Requirements

* C++17-capable compiler
* CMake 3.14+

## Build
Add this repository to your `.repos` file. For example:
```text
  aescape_utils_cpp:
    type: git
    url: git@github.com:aescape-inc/aescape_utils_cpp.git
    version: develop
```

Now you can build as usual. Most of the libraries in this repository will be usable with or without ROS.

### With ROS
```bash
colcon build --cmake-args -DCMAKE_BUILD_TYPE=<desired_build_type>
```

### Without ROS
```bash
cmake -S <path_to_source_directory> -B <path_to_build_directory> -DCMAKE_BUILD_TYPE=<desired_build_type>
cmake --build <path_to_build_directory> --parallel `nproc` --target install
```

If the build type is unspecified all libraries will be built using `RelWithDebInfo`.
