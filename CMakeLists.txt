# CMake shim to make custom shields discoverable by Zephyr/ZMK
cmake_minimum_required(VERSION 3.20.0)

# Add the local shields directory
list(APPEND SHIELD_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/config/boards/shields)
