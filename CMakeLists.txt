cmake_minimum_required(VERSION 3.14)

project(multibranch-sample-app)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include(FetchContent)
FetchContent_Declare(
    googletest
    # Specify the commit you depend on and update it regularly.
    URL https://github.com/google/googletest/archive/03597a01ee50ed33e9dfd640b249b4be3799d395.zip
)
# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

add_executable(multibranch-sample-app
    # Source files
    src/main.cpp
    # Header files
)

enable_testing()

add_executable(multibranch-sample-app-test
    # Source files
    test/sample-test.cpp
    # Header files
)

target_link_libraries(
    multibranch-sample-app-test
    GTest::gtest_main
)

include(GoogleTest)
gtest_discover_tests(multibranch-sample-app-test)
