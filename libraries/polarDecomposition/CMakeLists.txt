SET(SRC_FILES
	polarDecomposition.cpp
	polarDecompositionGradient.cpp
	polarDecompositionGradientDriver.cpp)
SET(INC_FILES
	polarDecomposition.h
	polarDecompositionGradient.h)

ADD_LIBRARY(polarDecomposition STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(polarDecomposition minivector)
