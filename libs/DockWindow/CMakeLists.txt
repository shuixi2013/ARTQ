set(TARGET_NAME DockWindow)

FILE(GLOB_RECURSE TARGET_SRC ${CMAKE_CURRENT_SOURCE_DIR}/*.c* ${CMAKE_CURRENT_SOURCE_DIR}/*.h* ${ART_INCLUDE_DIR}/${TARGET_NAME}/*.h)

add_library(${TARGET_NAME} STATIC ${TARGET_SRC})
target_link_libraries(${TARGET_NAME} Utils)
qt5_use_modules(${TARGET_NAME} Quick Widgets)
