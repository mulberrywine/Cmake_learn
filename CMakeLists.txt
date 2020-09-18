cmake_minimum_required(VERSION 2.8.3)
project(stage_ros)

include_directories(bt_nodes/include/micros_common_msg micros_bt/include/tree_manager simulation/stage_ros/Stage/libstage
)

aux_source_directory(bt_nodes/include/micros_common_msg MIC_MSG_SRC_LIST)

aux_source_directory(simulation/stage_ros/Stage/libstage STAGE_SRC_LIST)

aux_source_directory(micros_bt/include/tree_manager BBOARD_SRC_LIST)

set (EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

add_executable(stageros src/stageros.cpp ${MIC_MSG_SRC_LIST} ${STAGE_SRC_LIST} ${BBOARD_SRC_LIST})

