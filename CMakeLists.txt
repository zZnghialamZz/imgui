project(imgui)

set(IMGUI_INCLUDE_DIR "${CMAKE_CURRENT_LIST_DIR}")
set(IMGUI_SRC_DIR "${CMAKE_CURRENT_LIST_DIR}")

set(SOURCES
    "${IMGUI_SRC_DIR}/imgui_widgets.cpp"
    "${IMGUI_SRC_DIR}/imgui_tables.cpp"
    "${IMGUI_SRC_DIR}/imgui_demo.cpp"
    "${IMGUI_SRC_DIR}/imgui_draw.cpp"
    "${IMGUI_SRC_DIR}/imgui.cpp"
    )

set(HEADERS
    "${IMGUI_INCLUDE_DIR}/imgui_internal.h"
    "${IMGUI_INCLUDE_DIR}/imstb_rectpack.h"
    "${IMGUI_INCLUDE_DIR}/imstb_textedit.h"
    "${IMGUI_INCLUDE_DIR}/imstb_truetype.h"
    "${IMGUI_INCLUDE_DIR}/imconfig.h"
    "${IMGUI_INCLUDE_DIR}/imgui.h"
    )

include_directories(${IMGUI_INCLUDE_DIR})

add_library(imgui STATIC ${SOURCES} ${HEADERS})
