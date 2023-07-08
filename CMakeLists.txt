CMAKE_MINIMUM_REQUIRED(VERSION 3.9)

project(TestVulkan)

set(VulkanPath $ENV{VK_SDK_PATH})

include_directories(${VulkanPath}/Include)
link_directories(${VulkanPath}/Lib)
include_directories(3rd/glfw/include)
link_directories(3rd/glfw/lib)

add_executable(${PROJECT_NAME} main.cpp)
TARGET_LINK_LIBRARIES(${PROJECT_NAME} glfw3)
TARGET_LINK_LIBRARIES(${PROJECT_NAME} vulkan-1)

