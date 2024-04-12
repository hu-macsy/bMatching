cmake_minimum_required(VERSION 3.12)
project(bMatching CXX)

find_package(OpenMP)

add_executable(bMatching bMatching.cpp bSuitor.cpp bSuitorD.cpp mtxReader.cpp)
target_include_directories(bMatching PUBLIC "${PROJECT_SOURCE_DIR}/.")
target_link_libraries(bMatching PUBLIC OpenMP::OpenMP_CXX)
install(TARGETS bMatching DESTINATION ${CMAKE_INSTALL_PREFIX})
