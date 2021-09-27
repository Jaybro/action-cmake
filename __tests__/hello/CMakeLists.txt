cmake_minimum_required(VERSION 3.12)

project(hello)

add_executable(${PROJECT_NAME} ${PROJECT_NAME}.cpp)
set_target_properties(${PROJECT_NAME} PROPERTIES EXPORT_NAME ${PROJECT_NAME})

set(PROJECT_PACKAGE_TARGETS_NAME ${PROJECT_NAME}Targets)
install(TARGETS ${PROJECT_NAME} EXPORT ${PROJECT_PACKAGE_TARGETS_NAME})
