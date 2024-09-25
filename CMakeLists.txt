cmake_minimum_required(VERSION 3.10)
project(VulkanTriangle)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)

add_executable(VulkanTriangle main.cpp)

target_include_directories(VulkanTriangle PRIVATE ${Vulkan_INCLUDE_DIRS})
target_link_libraries(VulkanTriangle PRIVATE ${Vulkan_LIBRARIES} glfw)

