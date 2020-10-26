cmake_minimum_required(VERSION 3.10)
set(DEVELOPMENT_DIR /home/jmjatlanta/Development )
set(CMAKE_TOOLCHAIN_FILE ${DEVELOPMENT_DIR}/cpp/Arduino-CMake-Toolchain/Arduino-toolchain.cmake)
set(CMAKE_C_COMPILER avr-gcc )
set(CMAKE_CXX_COMPILER avr-g++ )
set(CMAKE_CXX_EXTENSIONS OFF)

project( blinky )

add_executable( blinky Blink.cpp )
target_link_arduino_libraries( blinky AUTO_PUBLIC )