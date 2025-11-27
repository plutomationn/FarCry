cmake_minimum_required(VERSION 3.10)
project(FarCry LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(${CMAKE_SOURCE_DIR})

add_subdirectory(CryCommon)
add_subdirectory(CrySystem)
add_subdirectory(Cry3DEngine)
add_subdirectory(CryGame)
add_subdirectory(CryNetwork)
add_subdirectory(Renderer)
add_subdirectory(LuaScriptSystem)
add_subdirectory(SoundSystem)

add_executable(FarCry FARCRY/Main.cpp)

target_link_libraries(FarCry
    CryGame
    Cry3DEngine
    CryCommon
    CrySystem
    CryNetwork
    Renderer
    LuaScriptSystem
    SoundSystem
)
