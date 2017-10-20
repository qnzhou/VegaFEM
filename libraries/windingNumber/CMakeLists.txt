SET(INC_FILES windingNumber.h)
SET(SRC_FILES windingNumber.cpp)

ADD_LIBRARY(windingNumber ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(windingNumber minivector objMesh)
