cmake_minimum_required(VERSION 3.5)

project(vulkanfun LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(vulkanfun main.cpp
    hellotriangleapplication.hpp hellotriangleapplication.cpp
    shaders/shader.vert
    shaders/shader.frag)

target_include_directories(vulkanfun PRIVATE
    /opt/homebrew/include
    /Users/alexps/VulkanSDK/1.3.250.0/macOS/include
)

target_link_directories(vulkanfun PRIVATE
    /opt/homebrew/lib
    /Users/alexps/VulkanSDK/1.3.250.0/macOS/lib
)

target_link_libraries(vulkanfun PRIVATE
    glfw
    vulkan
)
