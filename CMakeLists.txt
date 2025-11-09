cmake_minimum_required(VERSION 3.20.0)

# Make Zephyr treat this repo as a module
set(ZEPHYR_EXTRA_MODULES ${CMAKE_CURRENT_SOURCE_DIR})

# Register the custom shields directory
list(APPEND SHIELD_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/config/boards/shields)

