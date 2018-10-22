# Boost-CMake-Ubuntu-Linux
This repository demonstrates how to set up a boost library in a Ubuntu machine and use the CMake as a build system generator.

#CMake+Boost+Ubuntu+Linux
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

#Example
The example CMakeLists.txt contains the build instruction for including and linking the program_option component of boost.