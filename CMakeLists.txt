cmake_minimum_required(VERSION 3.20.0)

# Tell Zephyr to treat this repo as a shield module
list(APPEND SHIELD_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/config/boards/shields)
set(ZEPHYR_EXTRA_MODULES ${CMAKE_CURRENT_SOURCE_DIR})

