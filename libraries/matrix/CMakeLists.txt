SET(SRC_FILES
    example.cpp
    matrix.cpp
    matrixBLAS.cpp
    matrixBLASOptimized.cpp
    matrixBLASVanilla.cpp
    matrixExp.cpp
    matrixLAPACK.cpp
    matrixPCA.cpp
    matrixProjection.cpp)
SET(INC_FILES
    expokit_xgpadm.h
    matrix.h
    matrixBLAS.h
    matrixExp.h
    matrixLAPACK.h
    matrixPCA.h
    matrixProjection.h)

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})
ADD_LIBRARY(matrix STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(matrix matrixIO)
