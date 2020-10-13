cmake_minimum_required(VERSION 3.5)
project(base_msgs)

find_package(catkin REQUIRED)
find_package(message_generation REQUIRED)
find_package(std_msgs REQUIRED)

add_message_files(FILES Base.msg)

generate_messages(DEPENDENCIES std_msgs)


catkin_package(
	CATKIN_DEPENDS message_runtime std_msgs)
