# glad
if(NOT EMSCRIPTEN)
    add_subdirectory(glad/cmake)
    glad_add_library(glad STATIC LOADER LANGUAGE C API gl:core=2.1 wgl=1.0)
endif()

# glm
add_subdirectory(glm)

# jsoncpp
option(JSONCPP_WITH_TESTS "Compile and (for jsoncpp_check) run JsonCpp test executables" OFF)
option(JSONCPP_WITH_POST_BUILD_UNITTEST "Automatically run unit-tests as a post build step" OFF)
option(JSONCPP_WITH_STRICT_ISO "Issue all the warnings demanded by strict ISO C and ISO C++" OFF)
option(JSONCPP_WITH_PKGCONFIG_SUPPORT "Generate and install .pc files" OFF)
option(JSONCPP_WITH_CMAKE_PACKAGE "Generate and install cmake package files" OFF)
option(BUILD_SHARED_LIBS "Build jsoncpp_lib as a shared library." OFF)
option(BUILD_OBJECT_LIBS "Build jsoncpp_lib as a object library." OFF)
add_subdirectory(jsoncpp)

# lua
add_subdirectory(lua)
