file(GLOB_RECURSE SRC "*.cpp" "*.h")

add_library(CryGame STATIC ${SRC})

target_include_directories(CryGame PUBLIC
    ${CMAKE_SOURCE_DIR}
)

target_link_libraries(CryGame
    Cry3DEngine
    CrySystem
    CryCommon
)
