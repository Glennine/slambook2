cmake_minimum_required( VERSION 2.8 )
project(rgbd)
find_package(Sophus REQUIRED)
include_directories(${Sophus_INCLUDE_DIRS} ${OpenCV-INCLUDE_DIRS})
include_directories("/usr/local/include/eigen3")
set(Pangolin_DIR /home/g/C++_library/Pangolin/build)
find_package(Pangolin REQUIRED)
find_package(OpenCV REQUIRED)
add_executable(joinMap joinMap.cpp)
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES} ${OpenCV_LIBS} fmt)