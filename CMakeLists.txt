cmake_minimum_required(VERSION 3.13)

# initialize the SDK based on PICO_SDK_PATH
# note: this must happen before project()
include(pico_sdk_import.cmake)

project(spotwelderpico C CXX)

set(CMAKE_C_STANDARD 23)
set(CMAKE_C_STANDARD_REQUIRED FALSE)

pico_sdk_init()

add_executable(spotwelderpico
    spotwelderpico.c
)

# Add pico_stdlib library which aggregates commonly used features
target_link_libraries(spotwelderpico pico_stdlib)

# create map/bin/hex/uf2 file in addition to ELF.
pico_add_extra_outputs(spotwelderpico)

pico_enable_stdio_uart(spotwelderpico 0)
pico_enable_stdio_usb(spotwelderpico 1)
