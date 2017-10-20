ADD_EXECUTABLE(tetMesher tetMesher.cpp)
TARGET_LINK_LIBRARIES(tetMesher getopts objMesh mesher volumetricMesh
    ${OPENGL_LIBRARIES})

