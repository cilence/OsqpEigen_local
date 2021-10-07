cmake_minimum_required(VERSION 3.10)
project(osqp_eigen)

include_directories(./)
include_directories(./../third_party)
include_directories(./../third_party/osqp/include/osqp)

link_directories(./../third_party/osqp/lib)

aux_source_directory(./ SRCS_OSQP_EIGEN)
add_library(osqpeigen ${SRCS_OSQP_EIGEN})
target_link_libraries(osqpeigen osqp.a dl)