# CMakeLists.txt

# Minimum required version of CMake
cmake_minimum_required(VERSION 3.22)

# Project name
project(MSP_INTERFACE)

add_library(MSP_INTERFACE INTERFACE)

# Configura las variables de inclusión
target_include_directories(MSP_INTERFACE INTERFACE
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)

# Instala los archivos de encabezado
install(DIRECTORY include/ DESTINATION include)
