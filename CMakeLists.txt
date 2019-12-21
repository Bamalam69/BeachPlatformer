cmake_minimum_required(VERSION 3.14)
project(Platformer)

set(CMAKE_CXX_STANDARD 17)

set(SFML_STATIC_LIBRARIES TRUE)

find_package(SFML 2.5 COMPONENTS graphics system REQUIRED)

add_executable(Platformer Engine/main.cpp Engine/Entities/BaseEntity.cpp Engine/Entities/BaseEntity.h Engine/GameStates/GameState.cpp Engine/GameStates/GameState.h Engine/GameStates/GameStateSingleplayer.cpp Engine/GameStates/GameStateSingleplayer.h Engine/Utility/Vector2F.cpp Engine/Utility/Vector2F.h Engine/InputManager.cpp Engine/InputManager.h Engine/Utility/Random.cpp Engine/Utility/Random.h Engine/Game.cpp Engine/Game.h Engine/main.cpp)

target_link_libraries(Platformer sfml-graphics sfml-system)