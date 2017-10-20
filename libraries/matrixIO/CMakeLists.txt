SET(SRC_FILES
	matrixIO.cpp
	multiMatrixIO.cpp)

SET(INC_FILES
	matrixIO.h
	matrixMacros.h
	multiMatrixIO.h)

ADD_LIBRARY(matrixIO STATIC ${SRC_FILES} ${INC_FILES})
