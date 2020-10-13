cmake_minimum_required(VERSION 3.5)
project(pkg_app)

find_package(catkin)
find_package(pkg_downstream)

catkin_package(CATKIN_DEPENDS pkg_downstream
        LIBRARIES ${PROJECT_NAME})

add_library(${PROJECT_NAME} src/empty.cc)
add_dependencies(${PROJECT_NAME} ${catkin_EXPORTED_TARGETS})
