cmake_minimum_required(VERSION 3.25.0)

project(Treeland
    VERSION 0.7.0
    LANGUAGES CXX C)

set(CMAKE_INCLUDE_CURRENT_DIR ON) #use current cmake dir also as headers include dirs
set(CMAKE_EXPORT_COMPILE_COMMANDS ON) #generate build commands which helps tools like for example VSC to properly analyze project?
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Standard installation paths
include(GNUInstallDirs)
# Macros
include(FeatureSummary)

include(cmake/DefineTarget.cmake)

option(WITH_SUBMODULE_WAYLIB "Use the waylib from git submodule" ON)
add_feature_info(submodule_waylib WITH_SUBMODULE_WAYLIB "Use waylib from submodule")

option(ADDRESS_SANITIZER "Enable address sanitizer" OFF)
add_feature_info(ASanSupport ADDRESS_SANITIZER "https://github.com/google/sanitizers/wiki/AddressSanitizer")














































find_package(PkgConfig REQUIRED)
find_package(Qt6 CONFIG REQUIRED Core DBus Gui Qml Quick QuickControls2 LinguistTools Test QuickTest)









































add_subdirectory(src)


























