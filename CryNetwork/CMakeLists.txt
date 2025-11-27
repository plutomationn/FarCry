file(GLOB_RECURSE SRC "*.cpp" "*.h")

add_library(CryNetwork STATIC ${SRC})

target_include_directories(CryNetwork PUBLIC
    ${CMAKE_SOURCE_DIR}
)

target_link_libraries(CryNetwork
    CrySystem
    CryCommon
)
