file(GLOB_RECURSE SRC "*.cpp" "*.h")

add_library(CrySoundSystem STATIC ${SRC})

target_include_directories(CrySoundSystem PUBLIC
    ${CMAKE_SOURCE_DIR}
)

target_link_libraries(CrySoundSystem
    CrySystem
    CryCommon
)
