# Generated from qtquicktimeline.pro.

cmake_minimum_required(VERSION 3.16)

include(.cmake.conf)
project(QtQuickTimeline # special case
    VERSION "${QT_REPO_MODULE_VERSION}"
    DESCRIPTION "Qt Quick Timeline Libraries" # special case
    HOMEPAGE_URL "https://qt.io/"
    LANGUAGES CXX C
)

find_package(Qt6 ${PROJECT_VERSION} CONFIG REQUIRED COMPONENTS BuildInternals Core) # special case
find_package(Qt6 ${PROJECT_VERSION} QUIET CONFIG OPTIONAL_COMPONENTS Quick) # special case

if(NOT TARGET Qt::Quick)
    message(NOTICE "Skipping the build as the condition \"TARGET Qt::Quick\" is not met.")
    return()
endif()
qt_build_repo()
