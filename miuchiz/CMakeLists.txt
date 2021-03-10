cmake_minimum_required(VERSION 3.0.0)
set(LOCAL_PROJECT_NAME miuchiz)
project(${LOCAL_PROJECT_NAME} VERSION 0.1.0)

include_directories(../libmiuchiz-usb/include
                    ./include)

add_executable(${LOCAL_PROJECT_NAME} src/miuchiz.c
                                     src/actions/dump-flash.c
                                     src/actions/eject.c
                                     src/actions/load-flash.c
                                     src/actions/read-creditz.c
                                     src/actions/set-creditz.c
                                     src/actions/status.c)

target_link_libraries(${LOCAL_PROJECT_NAME} miuchiz-usb) 
INSTALL(TARGETS ${LOCAL_PROJECT_NAME} DESTINATION bin)
INSTALL(FILES completions/miuchiz DESTINATION share/bash-completion/completions)