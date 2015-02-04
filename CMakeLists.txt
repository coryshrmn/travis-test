cmake_minimum_required(VERSION 2.8.7 FATAL_ERROR)
project(travis-test)

foreach(p
    CMP0042 # MACOSX_RPATH
    )
    if(POLICY ${p})
        cmake_policy(SET ${p} NEW)
    endif()
endforeach()

add_executable(${PROJECT_NAME}
    src/hello.cpp
)
