CMAKE_MINIMUM_REQUIRED(VERSION 2.8.12)
PROJECT(VegaFEM)

SET(OPTIMIZATIONFLAG "-O2")
SET(OPENMPFLAG)
SET(CMAKE_CXX_FLAGS
    "${CMAKE_CXX_FLAGS} -Wall -Wno-write-strings ${OPTIMIZATIONFLAG} ${OPENMPFLAG}")
if(APPLE)
    SET(CXX_FLAGS "${CXX_FLAGS} -flax-vector-conversions")
endif(APPLE)
SET(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIC")

SET(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/libraries)
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/libraries/include)

FIND_PACKAGE(OpenGL)
INCLUDE_DIRECTORIES(${OPENGL_INCLUDE_DIR})

ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/clothBW)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/configFile)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/corotationalLinearFEM)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/distanceField)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/getopts)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/graph)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/hashTable)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/imageIO)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/matrix)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/matrixIO)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/mesher)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/minivector)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/objMesh)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/performanceCounter)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/polarDecomposition)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/sparseMatrix)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/sparseSolver)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/volumetricMesh)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/wildMagic/geometryQuery)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/wildMagic/meshKey)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/wildMagic/rational)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libraries/windingNumber)

#ADD_LIBRARY(VegaFEM clothBW configFile corotationalLinearFEM
#    distanceField graph hashTable imageIO matrix matrixIO mesher minivector
#    objMesh performanceCounter polarDecomposition sparseMatrix sparseSolver
#    volumetricMesh geometryQuery meshKey rational windingNumber)

ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/utilities/tetMesher)
