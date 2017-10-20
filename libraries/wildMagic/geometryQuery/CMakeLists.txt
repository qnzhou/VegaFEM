SET(INC_FILES
	query.h
	verticesQuery.h
	verticesQueryFiltered.h
	verticesQueryRational.h)

SET(SRC_FILES
	verticesQuery.cpp
	verticesQueryFiltered.cpp
	verticesQueryRational.cpp)

ADD_LIBRARY(geometryQuery ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(geometryQuery minivector meshKey rational)
