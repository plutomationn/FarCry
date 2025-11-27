file(GLOB_RECURSE SRC "*.cpp" "*.h")

add_library(CryScriptSystem STATIC ${SRC})

target_include_directories(CryScriptSystem PUBLIC
    ${CMAKE_SOURCE_DIR}
)

target_link_libraries(CryScriptSystem
    CrySystem
    CryCommon
)
