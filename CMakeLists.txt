# CMakeList.txt: проект CMake для CMakeProject2; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)

project ("CMakeProject2")

# Добавьте источник в исполняемый файл этого проекта.
add_executable (CMakeProject2 "src/main.cpp" "src/main.h" "src/player.h")
target_link_libraries(CMakeProject2 ${CMAKE_SOURCE_DIR}/3rdparty/sfml/library/sfml-graphics.lib)
target_link_libraries(CMakeProject2 ${CMAKE_SOURCE_DIR}/3rdparty/sfml/library/sfml-audio.lib)
target_link_libraries(CMakeProject2 ${CMAKE_SOURCE_DIR}/3rdparty/sfml/library/sfml-network.lib)
target_link_libraries(CMakeProject2 ${CMAKE_SOURCE_DIR}/3rdparty/sfml/library/sfml-system.lib)
target_link_libraries(CMakeProject2 ${CMAKE_SOURCE_DIR}/3rdparty/sfml/library/sfml-window.lib)

include_directories(${CMAKE_SOURCE_DIR}/3rdparty/sfml/include)

set_property(TARGET CMakeProject2 PROPERTY CXX_STANDART_17)
set_property(TARGET CMakeProject2 PROPERTY CXX_STANDART_REQUIRED ON)

# TODO: Добавьте тесты и целевые объекты, если это необходимо.
