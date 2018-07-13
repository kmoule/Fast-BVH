cmake_minimum_required(VERSION 3.8)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(FastBVH CXX)

set(SOURCES
    BBox.cpp
    BVH.cpp
)

set(HEADERS
    BBox.h
    BVH.h
    IntersectionInfo.h
    Log.h
    Object.h
    Ray.h
    Stopwatch.h
    Vector3.h
)

add_library(FastBVH STATIC ${SOURCES})

install (TARGETS FastBVH DESTINATION lib)
install (FILES ${HEADERS} DESTINATION include)

