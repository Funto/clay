cmake_minimum_required(VERSION 3.27)
project(clay)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

add_subdirectory("examples/cpp-project-example")

# Don't try to compile C99 projects using MSVC
if(NOT MSVC)
  add_subdirectory("examples/raylib-sidebar-scrolling-container")
  add_subdirectory("examples/raylib-multi-context")
#  add_subdirectory("examples/cairo-pdf-rendering") Some issue with github actions populating cairo, disable for now
  add_subdirectory("examples/clay-official-website")
  add_subdirectory("examples/introducing-clay-video-demo")
  add_subdirectory("examples/SDL2-video-demo")
endif()
