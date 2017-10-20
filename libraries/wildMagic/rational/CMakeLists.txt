SET(INC_FILES integer.h rVector.h rational.h)
SET(SRC_FILES integer.cpp rational.cpp)

ADD_LIBRARY(rational ${SRC_FILES} ${INC_FILES})
