# cross_compile_raspi

### Move to the build directory. 
cmake -DCMAKE_BUILD_TYPE=Release .. && make all

### Tele-operation for raspi such as Putty program.
ssh ubuntu@192.168.151.156

### Turn on the file expoloer
### Go to other locations
### type the sftp://192.168.151.156/ on the "connect to server" block.
sftp://192.168.151.156/


reference link: http://lablk.blogspot.com/2017/10/build-system-cmake-x8664-linux-arm-linux.

https://releases.linaro.org/components/toolchain/binaries/7.1-2017.08/aarch64-linux-gnu/
1. Install "gcc-linaro-7.1.1-2017.08-x86_64_aarch64-linux-gnu.tar.xz" from the above link and unzip at "/compiler_raspi4"
2. Make "toolchain.arm.cmake" file (refer to the reference link)
  : change CMAKE_SYSTEM_PROCESSOR and COMPILER_ROOT (SET(CMAKE_SYSTEM_PROCESSOR aarch64))
3. cmake -DCMAKE_TOOLCHAIN_FILE=toolchain.arm.cmake -DCMAKE_BUILD_TYPE=Release .. && make all
