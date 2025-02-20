cmake_minimum_required(VERSION 3.8) # 3.8+ supports C++17 features
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_compile_definitions(USE_ETCD)

include_directories(include)
add_subdirectory(include)
add_subdirectory(src)

install(TARGETS transfer_engine ARCHIVE DESTINATION lib)