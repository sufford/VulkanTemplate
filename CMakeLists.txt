cmake_minimum_required(VERSION 3.14)

project(VulkanTemplate)
find_package(Vulkan REQUIRED)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(VulkanTemplate src/main.cpp)

target_include_directories(VulkanTemplate PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/include")
target_link_libraries(VulkanTemplate PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/lib/lib-vc2017/glfw3.lib")
target_link_libraries(VulkanTemplate PRIVATE 
    "${CMAKE_CURRENT_SOURCE_DIR}/lib/lib-vc2017/glfw3.lib"
    Vulkan::Vulkan
)