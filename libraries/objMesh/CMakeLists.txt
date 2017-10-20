SET(SRC_FILES
	boundingBox.cpp
	objMesh-disjointSet.cpp
	objMesh.cpp
	objMeshBinaryLoader.cpp
	objMeshClose.cpp
	objMeshEncode.cpp
	objMeshGraph.cpp
	objMeshOctree.cpp
	objMeshOffsetVoxels.cpp
	objMeshOrientable.cpp
	objMeshRender.cpp
	octree.cpp
	simpleSphere.cpp
	triangle-closestPoint.cpp
	triangle.cpp
	tribox3.cpp)

SET(INC_FILES
	boundingBox.h
	objMesh-disjointSet.h
	objMesh.h
	objMeshBinaryLoader.h
	objMeshClose.h
	objMeshEncode.h
	objMeshGraph.h
	objMeshOctree.h
	objMeshOffsetVoxels.h
	objMeshOrientable.h
	objMeshRender.h
	octree.h
	simpleSphere.h
	triangle.h
	tribox3.h)

ADD_LIBRARY(objMesh STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(objMesh minivector matrixIO graph imageIO)
