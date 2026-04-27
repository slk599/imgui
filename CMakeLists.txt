cmake_minimum_required(VERSION 3.16)

# ── ImGui library target ──────────────────────────────────────────────────────
add_library(imgui STATIC
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
)

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Backends
target_sources(imgui PRIVATE
    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_opengl3.cpp
)

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/backends)
