set(IMGUI_SOURCE_DIRECTORY ../imgui)

add_library(imgui-sfml
    ${IMGUI_SOURCE_DIRECTORY}/imgui_draw.cpp
    ${IMGUI_SOURCE_DIRECTORY}/imgui_tables.cpp
    ${IMGUI_SOURCE_DIRECTORY}/imgui_widgets.cpp
    ${IMGUI_SOURCE_DIRECTORY}/imgui.cpp

    imgui-SFML.cpp
)

target_include_directories(imgui-sfml PUBLIC
    .
    ${IMGUI_SOURCE_DIRECTORY}
)

target_link_libraries(imgui-sfml PRIVATE
    SFML::Graphics
    SFML::Window
)