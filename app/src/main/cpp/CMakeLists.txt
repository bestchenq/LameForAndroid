
cmake_minimum_required(VERSION 3.4.1)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c99 -Wall")
#set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ../jniLibs/${ANDROID_ABI})
add_library(mp3lame-lib SHARED
            ./libmp3lame/bitstream.c
            ./libmp3lame/encoder.c
            ./libmp3lame/fft.c
            ./libmp3lame/gain_analysis.c
            ./libmp3lame/id3tag.c
            ./libmp3lame/lame.c
            ./libmp3lame/mpglib_interface.c
            ./libmp3lame/newmdct.c
            ./libmp3lame/presets.c
            ./libmp3lame/psymodel.c
            ./libmp3lame/quantize.c
            ./libmp3lame/quantize_pvt.c
            ./libmp3lame/reservoir.c
            ./libmp3lame/set_get.c
            ./libmp3lame/tables.c
            ./libmp3lame/takehiro.c
            ./libmp3lame/util.c
            ./libmp3lame/vbrquantize.c
            ./libmp3lame/VbrTag.c
            ./libmp3lame/version.c
            ./wrapper.c)



# Include libraries needed for SerialPort lib
target_link_libraries(mp3lame-lib
                      android
                      log)