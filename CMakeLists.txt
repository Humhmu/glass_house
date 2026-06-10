cmake_minimum_required(VERSION 4.3)
project(glass_house)


include(FetchContent)

FetchContent_Declare(
    raylib
    GIT_REPOSITORY https://github.com/raysan5/raylib.git
    GIT_TAG        6.0
    SOURCE_DIR     ${CMAKE_SOURCE_DIR}/lib/raylib   # lands in lib/
)

FetchContent_MakeAvailable(raylib)

add_executable(${PROJECT_NAME} src/main.c)
target_link_libraries(${PROJECT_NAME} raylib)
