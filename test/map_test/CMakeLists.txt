project(map_TEST)

add_executable(${PROJECT_NAME} map_TEST.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${PNC_Map_Dir})

target_link_libraries(${PROJECT_NAME} PUBLIC pnc_map)

add_test(
    NAME map_info_test
    COMMAND ${PROJECT_NAME}
)