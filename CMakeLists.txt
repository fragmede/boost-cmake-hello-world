CMAKE_MINIMUM_REQUIRED (VERSION 2.6)
PROJECT (MyProject)
set(EXECUTABLE_OUTPUT_PATH "${CMAKE_BINARY_DIR}/bin")

ADD_SUBDIRECTORY (src)
if(CMAKE_HOST_UNIX)
  SET (CMAKE_CXX_FLAGS "$ENV{CPPFLAGS} -O3")
  SET (CMAKE_C_FLAGS "$ENV{CPPFLAGS} -O3")
  SET (CMAKE_LD_FLAGS "$ENV{LDFLAGS}")
endif(CMAKE_HOST_UNIX)
