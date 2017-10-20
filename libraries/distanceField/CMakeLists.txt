SET(INC_FILES
    closestPointField.h
    distanceField.h
    distanceFieldBase.h
    distanceFieldCreator.h
    distanceFieldMT.h
    distanceFieldNarrowBand.h
    marchingCubes.h
    marchingCubesTable.h
    signedDistanceFieldFromPolygonSoup.h
    trilinearInterpolation.h)
SET(SRC_FILES
    closestPointField.cpp
    computeField.cpp
    computeFieldMT.cpp
    computeFieldNarrowBand.cpp
    distanceField.cpp
    distanceFieldBase.cpp
    distanceFieldCreator.cpp
    distanceFieldMT.cpp
    distanceFieldNarrowBand.cpp
    marchingCubes.cpp
    signedDistanceFieldFromPolygonSoup.cpp)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/libraries/objMesh)
ADD_LIBRARY(distanceField ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(distanceField
    objMesh hashTable minivector performanceCounter matrixIO configFile)
