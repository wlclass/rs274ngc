
IF(UNIX)
	SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Wextra")
ENDIF()

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)
ADD_LIBRARY(rs274ngc STATIC rs274ngc_errors.cc rs274ngc_pre.cc block.cpp types.cpp setup.cpp error.cpp ops.cpp arc.cpp)
TARGET_LINK_LIBRARIES(rs274ngc m)
