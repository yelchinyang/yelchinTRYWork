cmake_minimum_required(VERSION 2.8)
project(ARTIFACT)

set(CMAKE_CXX_FLAGS "-g3 -fPIC -Wall")
set(CMAKE_CXX_FLAGS_DEBUG "-g3 -fPIC -Wall")
set(CMAKE_CXX_FLAGS_RELEASE "-O2 -fPIC -Wall")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")


include_directories(./inc)
include_directories(./)

aux_source_directory(./src SRC_LIST)
#list(APPEND SRC_LIST ./src)

add_executable(ARTIFACT ${SRC_LIST})
#target_link_libraries(TestYoutuModule /data/home/yelchinyang/pyIncludeSO/youtu/TestYoutuModule/lib/libProductsDetector.so yopencv_core opencv_highgui z)


#target_link_libraries(ARTIFACT /data/home/yelchinyang/pyIncludeSO/youtu/artifact-release-04-13/lib/libProductsDetector.so  /usr/local/lib/libopencv_highgui.so.3.3.1 /usr/local/lib/libopencv_imgcodecs.so.3.3.1 /usr/local/lib/libopencv_imgproc.so.3.3 )



target_link_libraries(ARTIFACT /data/home/yelchinyang/pyIncludeSO/youtu/artifact-release-04-13/lib/libProductsDetector.so  /usr/local/lib/libopencv_highgui.so.3.3.1 /usr/local/lib/libopencv_imgcodecs.so.3.3.1 /usr/local/lib/libopencv_imgproc.so.3.3)

