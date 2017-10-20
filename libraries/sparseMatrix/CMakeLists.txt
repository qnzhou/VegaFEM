SET(SRC_FILES
	sparseMatrixMT.cpp
	sparseMatrix.cpp)

SET(INC_FILES
	sparseMatrixMT.h
	sparseMatrix.h)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/libraires/sparseSolver)
ADD_LIBRARY(sparseMatrix STATIC ${SRC_FILES} ${INC_FILES})
