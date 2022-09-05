cmake_minimum_required(VERSION 3.16)

set(CMAKE_C_STANDARD 99)

project(luaLib)

add_library(luaLib
    lapi.c
    lcode.c
    lctype.c
    ldebug.c
    ldo.c
    ldump.c
    lfunc.c
    lgc.c
    llex.c
	lmem.c
    lobject.c
    lopcodes.c
    lparser.c
    lstate.c
    lstring.c
    ltable.c
	ltm.c
    lundump.c
    lvm.c
    lzio.c
    ltests.c
    lauxlib.c
	lbaselib.c
    ldblib.c
    liolib.c
    lmathlib.c
    loslib.c
    ltablib.c
    lstrlib.c
	lutf8lib.c
    loadlib.c
    lcorolib.c
    linit.c
)

target_include_directories(luaLib PUBLIC .)
target_link_libraries(luaLib PUBLIC m)

project(lua)

add_executable(lua
    onelua.c
)

target_include_directories(lua PUBLIC .)
target_link_libraries(lua PUBLIC luaLib)