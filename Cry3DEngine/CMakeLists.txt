file(GLOB_RECURSE SRC "*.cpp" "*.h")

add_library(Cry3DEngine STATIC ${SRC})

target_include_directories(Cry3DEngine PUBLIC
    ${CMAKE_SOURCE_DIR}
)

target_link_libraries(Cry3DEngine
    CrySystem
    CryCommon
)
