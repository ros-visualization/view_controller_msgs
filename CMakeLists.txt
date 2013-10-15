cmake_minimum_required(VERSION 2.8.3)
project(view_controller_msgs)

set(MSG_DEPS
  std_msgs
  geometry_msgs)

find_package(catkin REQUIRED genmsg ${MSG_DEPS})

set(MSG_FILES
CameraPlacement.msg
)

add_message_files(DIRECTORY msg FILES ${MSG_FILES})

generate_messages(DEPENDENCIES ${MSG_DEPS})

catkin_package(DEPENDS ${MSG_DEPS})
