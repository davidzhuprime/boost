cmake_minimum_required(VERSION 3.16)
project(boost24)


find_package(Boost REQUIRED filesystem program_options regex timer) # header only libraries must not be added here


add_executable(boost24 main.cpp)
target_link_libraries(boost24 ${Boost_LIBRARIES} pthread boost_thread)
