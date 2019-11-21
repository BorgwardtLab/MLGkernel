FILE(GLOB SOURCES
  *.cpp
  ../utility/*.cpp
  ../matrices/matrices.cpp
)

INCLUDE_DIRECTORIES(
  ${CMAKE_SOURCE_DIR}/include
  ${CMAKE_SOURCE_DIR}/matrices
  ${CMAKE_SOURCE_DIR}/utility
  ${CMAKE_SOURCE_DIR}/utility/filetypes
)

ADD_EXECUTABLE( runMLG
  ${SOURCES}
)

TARGET_INCLUDE_DIRECTORIES( runMLG SYSTEM PUBLIC ${EIGEN3_INCLUDE_DIR} )
TARGET_LINK_LIBRARIES( runMLG Threads::Threads )
