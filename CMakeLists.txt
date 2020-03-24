# ================================================================

project(spark)

set(CurrentDir ${CMAKE_CURRENT_SOURCE_DIR})

# ================================================================

file(GLOB SRC_FILES
    ${CurrentDir}/src/Core/*.cpp
    ${CurrentDir}/src/Extensions/Emitters/*.cpp
    ${CurrentDir}/src/Extensions/Modifiers/*.cpp
    ${CurrentDir}/src/Extensions/Renderers/*.cpp
    ${CurrentDir}/src/Extensions/Zones/*.cpp
)

# ================================================================

include_directories(
    ${CurrentDir}/include
)

add_library(spark STATIC ${SRC_FILES})

# ================================================================