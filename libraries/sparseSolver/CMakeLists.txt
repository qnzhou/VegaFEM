SET(SRC_FILES
    ARPACKSolver.cpp
    PardisoSolver.cpp
    SPOOLESSolver.cpp
    SPOOLESSolverMT.cpp
    ZTAZMultiplicator.cpp
    invMKSolver.cpp
    invZTAZMSolver.cpp
    invZTAZSolver.cpp
    linearSolver.cpp
    CGSolver.cpp)
SET(INC_FILES
    ARPACKSolver.h
    PardisoSolver.h
    SPOOLESSolver.h
    SPOOLESSolverMT.h
    ZTAZMultiplicator.h
    invMKSolver.h
    invZTAZMSolver.h
    invZTAZSolver.h
    linearSolver.h
    sparseSolverAvailability.h
    sparseSolvers.h
    CGSolver.h)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/libraries/matrix)
ADD_LIBRARY(sparseSolver STATIC ${SRC_FILES} ${INC_FILES})
TARGET_LINK_LIBRARIES(sparseSolver sparseMatrix matrix)
