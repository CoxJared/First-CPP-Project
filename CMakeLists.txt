cmake_minimum_required(VERSION 3.15.1)
project(First-CPP-Project)

option(BUILD_TESTS "Turn on build for tests of First-CPP-Project" OFF)

file(GLOB SRC_FILES
        "src/*.cpp"
)

set(INC_FILES_DIR
        include/
)

if (BUILD_TESTS)
    add_subdirectory(test)
endif()

include_directories(
    ${INC_FILES_DIR}
)

add_executable(First-CPP-Project
        ${SRC_FILES}
)
