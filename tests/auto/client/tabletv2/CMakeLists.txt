# Generated from tabletv2.pro.

#####################################################################
## tst_tabletv2 Test:
#####################################################################

qt_internal_add_test(tst_tabletv2
    SOURCES
        ../shared/corecompositor.cpp ../shared/corecompositor.h
        ../shared/coreprotocol.cpp ../shared/coreprotocol.h
        ../shared/datadevice.cpp ../shared/datadevice.h
        ../shared/mockcompositor.cpp ../shared/mockcompositor.h
        ../shared/textinput.cpp ../shared/textinput.h
        ../shared/xdgoutputv1.cpp ../shared/xdgoutputv1.h
        ../shared/xdgshell.cpp ../shared/xdgshell.h
        tst_tabletv2.cpp
    INCLUDE_DIRECTORIES
        ../shared
    PUBLIC_LIBRARIES
        Qt::Gui
        Qt::OpenGL
        Qt::WaylandClientPrivate
        Wayland::Server
        Threads::Threads # special case
)

qt6_generate_wayland_protocol_server_sources(tst_tabletv2
    FILES
        ${CMAKE_CURRENT_SOURCE_DIR}/../../../../src/3rdparty/protocol/tablet-unstable-v2.xml
        ${CMAKE_CURRENT_SOURCE_DIR}/../shared/../../../../src/3rdparty/protocol/text-input-unstable-v2.xml
        ${CMAKE_CURRENT_SOURCE_DIR}/../shared/../../../../src/3rdparty/protocol/wayland.xml
        ${CMAKE_CURRENT_SOURCE_DIR}/../shared/../../../../src/3rdparty/protocol/xdg-output-unstable-v1.xml
        ${CMAKE_CURRENT_SOURCE_DIR}/../shared/../../../../src/3rdparty/protocol/xdg-shell.xml
)
