SET(SRC_FILES
	corotationalLinearFEMMT.cpp
	corotationalLinearFEM.cpp)
SET(INC_FILES
	corotationalLinearFEM.h
	corotationalLinearFEMMT.h)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/libraries/polarDecomposition/)
ADD_LIBRARY(corotationalLinearFEM STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(corotationalLinearFEM polarDecomposition volumetricMesh
	sparseMatrix)
