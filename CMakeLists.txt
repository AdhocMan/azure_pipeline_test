cmake_minimum_required(VERSION 3.8 FATAL_ERROR) # 3.8 added CUDA language support without FindCUDA
project(azure_test LANGUAGES CXX VERSION 0.9.1)

find_package(MPI REQUIRED)
add_executable(main main.cpp)
add_executable(main_fail main_fail.cpp)
target_link_libraries(main MPI::MPI_CXX)
target_link_libraries(main_fail MPI::MPI_CXX)
