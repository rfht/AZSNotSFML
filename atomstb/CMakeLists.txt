# AtomSTB CMake File
# Written by Ethan "flibitijibibo" Lee
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT(AtomSTB)

IF (APPLE)
	SET(CMAKE_OSX_ARCHITECTURES i386 x86_64)
	SET(CMAKE_OSX_DEPLOYMENT_TARGET 10.6)
ENDIF()

# Compiler flags
SET(CMAKE_C_FLAGS "-O2 -I/usr/include/sys")

# Target
ADD_LIBRARY(atomstb SHARED atomstb.c)
