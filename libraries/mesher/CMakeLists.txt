SET(SRC_FILES
    delaunayMesher.cpp
    isosurfaceMesher.cpp
    tetMesher.cpp
    triangleTetIntersection.cpp)
SET(INC_FILES
    delaunayMesher.h
    isosurfaceMesher.h
    tetMesher.h
    triangleTetIntersection.h)

ADD_LIBRARY(mesher ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(mesher distanceField minivector objMesh volumetricMesh
    windingNumber performanceCounter geometryQuery meshKey rational)
