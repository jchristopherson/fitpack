# Locate the source directory
set(dir ${CMAKE_CURRENT_SOURCE_DIR})

# Define the source files
set(FITPACK_SOURCES
    ${dir}/fitpack_core.f90
    ${dir}/fitpack.f90
)
set(FITPACK_SOURCES ${FITPACK_SOURCES} PARENT_SCOPE)