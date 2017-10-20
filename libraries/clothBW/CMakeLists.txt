SET(SRC_FILES
	clothBW.cpp
	clothBWFromObjMesh.cpp
	clothBWMT.cpp)
SET(INC_FILES
	clothBW.h
	clothBWFromObjMesh.h
	clothBWMT.h)

ADD_LIBRARY(clothBW STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(clothBW minivector objMesh sparseMatrix)
