# Automated test demo

This is a minimal example that uses googletest and CMake in order to instrument
the code with autoamted tests.

Some features

  * CMake functionality for testing
  * googletest framework as git submodule
  * For Travis CI support see `.travis.yaml` file


## Building with tests

  ```
cd <project_path>
git submodule update --init  # To checkout googletest

mkdir build
cd build
cmake ../
make
ctest
  ```

### Some rationale for git submodule

In order to build this package you will need to checkout googletest which is
necessary to compile the test source code. I have tried several approaches to
googletest/gtest including OS package manager, git and `ExternalProject` of
CMake. In my opinion the most reliable is to incoroprate googletest as git
submodule. `External Project` did require some configuration and had to che


## Some literature

"Working Effectively with Legacy Code" by Michael C. Feathers
