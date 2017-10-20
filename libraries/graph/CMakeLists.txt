SET(SRC_FILES graph.cpp)
SET(INC_FILES graph.h)

ADD_LIBRARY(graph STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(graph minivector matrixIO sparseMatrix)
