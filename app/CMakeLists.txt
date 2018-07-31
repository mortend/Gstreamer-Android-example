cmake_minimum_required(VERSION 3.4.1)

include_directories(${GST_DIR}/include/gstreamer-1.0)
include_directories(${GST_DIR}/include/glib-2.0)
include_directories(${GST_DIR}/lib/glib-2.0/include)
link_directories(${GST_DIR}/lib)

add_library(tutorial-5 SHARED
    src/main/cpp/tutorial-5.c)

target_link_libraries(tutorial-5 log android
    ${GST_DIR}/lib/libgstreamer_android.so)
