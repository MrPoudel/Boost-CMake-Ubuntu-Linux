# Boost-CMake-Ubuntu-Linux
This repository demonstrates how to set up a boost library in a Ubuntu machine and use CMake as a build system generator.

# This repository demonstrates how to include and link boost library from cmake.

Prerequisite:
I assume that you have already installed the latest boost library in your machine correctly.
if not, 
1. download the latest boost library from : https://www.boost.org/users/history/version_1_67_0.html
2. extract the boost library to the the desired location using: tar --bzip2 -xf /path/to/boost_1_67_0.tar.bz2
3. go to the extracted directory: cd /path/to/boost_1_67_0
4. ./bootstrap.sh --prefix=/usr/local
5. sudo ./b2 install

After these steps boost library headers will be installed on /usr/local/include and compiled libraries will be installed on /usr/local/lib directory.

# Example
This project shows two examples using boost library. The first one, header_only.cpp needs header only boost library and the second one, boost_program_option.cpp needs a pre-compiled libboost_program_options library to be linked.

# Out-of-source build

```
create a directory called build in projects's root directory
navigate to the build directory 
Turn ON ENABLE_EXAMPLES
Make the project
```
