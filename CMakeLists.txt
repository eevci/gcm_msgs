cmake_minimum_required(VERSION 3.0.2)
project(gcm_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_service_files( FILES
    CreateUDPComm.srv
    CreateTCPComm.srv
    CreateRS232Comm.srv
)

add_message_files( FILES
    NetworkMessage.msg
)
generate_messages(DEPENDENCIES
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
  )