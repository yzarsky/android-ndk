cmake_minimum_required(VERSION 3.4.1)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Werror")
set(echo_SRCS debug_utils.cpp
              audio_common.cpp
              audio_player.cpp
              audio_recorder.cpp
              audio_main.cpp)
add_library(echo SHARED ${echo_SRCS})

# Include libraries needed for hello-jni lib
target_link_libraries(echo android log OpenSLES atomic)
