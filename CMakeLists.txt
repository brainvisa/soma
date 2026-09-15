cmake_minimum_required(VERSION 4.4)

# Nom du projet principal
project(soma VERSION 6.0.19 LANGUAGES C CXX Fortran)

# Configuration générale
set(CMAKE_MODULE_PATH "$ENV{PIXI_PROJECT_ROOT}/lib/cmake/brainvisa-cmake" ${CMAKE_MODULE_PATH})

find_package(brainvisa-cmake REQUIRED)

add_subdirectory(brainvisa-share)
add_subdirectory(soma-io)
add_subdirectory(aims-free)
add_subdirectory(aims-gpl)

# Message de confirmation
message(STATUS "Configuration de SOMA terminée")
message(STATUS "Version: ${PROJECT_VERSION}")
message(STATUS "Sous-projets inclus: brainvisa-share, soma-io, aims-free, aims-gpl")
