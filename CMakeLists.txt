cmake_minimum_required(VERSION 3.14)
project(Auto_Vk_Starter)

set(CMAKE_CXX_STANDARD 20)

add_executable(Auto_Vk_Starter src/main.cpp)

# Auto-Vk
include(cmake/avk.cmake)
target_link_libraries(${PROJECT_NAME} PUBLIC avk)

# Vulkan
find_package(Vulkan REQUIRED)
target_link_libraries(${PROJECT_NAME} PUBLIC Vulkan::Vulkan)
