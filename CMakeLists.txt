cmake_minimum_required(VERSION 3.10)

project(OsqpEigen-Example)
set (CMAKE_CXX_STANDARD 14)


add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/include)

include_directories(./include)
include_directories(./third_party)
include_directories(./third_party/osqp/include/osqp)

link_directories(./third_party/osqp/lib)
add_executable(MPC MPC.cpp)
target_link_libraries(MPC osqpeigen osqp.a dl)