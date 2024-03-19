cmake_minimum_required(VERSION 3.25.1)
project(VulkanTest)

find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)

include_directories(${Vulkan_INCLUDE_DIRS})
include_directories(${GLFW_INCLUDE_DIRS})

add_executable(VulkanTest main.cpp)

target_link_libraries(VulkanTest ${Vulkan_LIBRARIES} glfw)