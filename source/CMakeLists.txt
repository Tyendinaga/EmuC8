set(SOURCES main.cpp 
            cpu/chip8.cpp
            display/display.cpp
            display/glad.c)

set (HEADERS cpu/chip8.hpp
            display/display.hpp
            display/glad.h)

add_executable(EmuC8 ${SOURCES} ${HEADERS})

include_directories(cpu display)

target_link_libraries(EmuC8 ${OPENGL_LIBRARIES})
target_link_libraries(EmuC8 ${GLFW_STATIC_LIBRARIES})
target_link_libraries(EmuC8 pthread)
target_link_libraries(EmuC8 ${X11_LIBRARIES})