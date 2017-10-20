SET(SRC_FILES
	imageIO.cpp)

SET(INC_FILES
	imageFormats.h
	imageIO.h)

ADD_LIBRARY(imageIO STATIC ${SRC_FILES} ${INC_FILES})
