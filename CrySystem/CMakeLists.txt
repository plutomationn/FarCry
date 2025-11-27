file(GLOB_RECURSE SRC "*.cpp" "*.h")

add_library(CrySystem STATIC ${SRC})

target_include_directories(CrySystem PUBLIC
    ${CMAKE_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(CrySystem
    CryCommon
)
