cmake_minimum_required(VERSION 3.8)
project (soma LANGUAGES C CXX Fortran)
set( NO_BV_MAKER TRUE)
set(CMAKE_MODULE_PATH "$ENV{PIXI_PROJECT_ROOT}/lib/cmake/brainvisa-cmake:$ENV{PIXI_PROJECT_ROOT}/lib/cmake/brainvisa-cmake/modules" ${CMAKE_MODULE_PATH})
find_package( brainvisa-cmake REQUIRED )

BRAINVISA_PROJECT()
enable_testing()

set(DESIRED_QT_VERSION 5)

add_subdirectory(brainvisa-share)
add_subdirectory(soma-io)
add_subdirectory(aims-free)
add_subdirectory(aims-gpl)

# Message de confirmation
message(STATUS "Configuration de SOMA terminée")
message(STATUS "Version: ${PROJECT_VERSION}")
message(STATUS "Sous-projets inclus: brainvisa-share, soma-io, aims-free, aims-gpl")
