SET(SRC_FILES
	eig3.cpp
	mat3d.cpp
	vec2d.cpp
	vec3.cpp
	vec3d.cpp)

SET(INC_FILES
	eig3.h
	mat3d.h
	minivector.h
	vec2d.h
	vec3.h
	vec3d.h)

ADD_LIBRARY(minivector STATIC ${SRC_FILES} ${INC_FILES})
