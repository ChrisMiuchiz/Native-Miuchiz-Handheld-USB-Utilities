cmake_minimum_required(VERSION 3.0.0)
project(miuchiz-usb VERSION 0.1.0 LANGUAGES C)
include_directories(include)
add_library(miuchiz-usb src/libmiuchiz-usb.c
                        src/commands.c
                        src/timer.c)
set_property(TARGET miuchiz-usb PROPERTY C_STANDARD 11)