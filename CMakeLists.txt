cmake_minimum_required(VERSION 3.16)
project(boost24)

#set(ENV{BOOST_DIR} "C:\\local\\boost_1_80_0")
#set(ENV{BOOST_DIR} "C:\\Users\\david\\Documents\\workspace\\boost_1_81_0")
#set(ENV{Boost_INCLUDE_DIR} ${BOOST_DIR}\\boost)

#find_package(Boost REQUIRED filesystem program_options regex timer) # header only libraries must not be added here
find_package(OpenCV REQUIRED)
find_package(Boost REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(${Boost_INCLUDE_DIR})
link_directories("C:\\local\\boost_1_80_0\\lib64-msvc-14.3")

add_executable(boost24 main.cpp)
target_link_libraries(boost24 ${Boost_LIBRARIES} ${OpenCV_LIBS})
