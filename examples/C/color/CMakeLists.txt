#  minimum required cmake version: 3.1.0
cmake_minimum_required(VERSION 3.1.0)

project(RealsenseExamples-Color)

# Save the command line compile commands in the build output
set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

add_executable(rs-color rs-color.c ../example.h)
target_link_libraries(rs-color ${DEPENDENCIES})
set_target_properties (rs-color PROPERTIES
FOLDER "Examples/C"
)

install(
TARGETS

rs-color

RUNTIME DESTINATION
${CMAKE_INSTALL_PREFIX}/bin
)

