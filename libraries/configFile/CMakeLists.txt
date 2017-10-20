SET(SRC_FILES configFile.cpp)
SET(INC_FILES configFile.h)

ADD_LIBRARY(configFile STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(configFile minivector)
