cmake_minimum_required(VERSION 3.17)

project(lua)

set(target_name lua)
add_library(${target_name} STATIC)
target_include_directories(${target_name} PRIVATE .)
target_sources(${target_name} PRIVATE
    lapi.c lcode.c lctype.c ldebug.c ldo.c ldump.c lfunc.c lgc.c llex.c
	lmem.c lobject.c lopcodes.c lparser.c lstate.c lstring.c ltable.c
	ltm.c lundump.c lvm.c lzio.c ltests.c
    lauxlib.c
    lbaselib.c ldblib.c liolib.c lmathlib.c loslib.c ltablib.c lstrlib.c 
	lutf8lib.c loadlib.c lcorolib.c linit.c
)