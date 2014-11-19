#
# drivers/caris
#
set(PDAL_CARIS_PATH drivers/caris)
set(PDAL_CARIS_HEADERS "${PDAL_HEADERS_DIR}/${PDAL_CARIS_PATH}")
set(PDAL_CARIS_SRC "${PROJECT_SOURCE_DIR}/src/${PDAL_CARIS_PATH}")

set(PDAL_DRIVERS_CARIS_HPP
  "${PDAL_CARIS_HEADERS}/CloudReader.hpp"
  "${PDAL_CARIS_SRC}/Utils.hpp"
  "${PDAL_CARIS_SRC}/config.h"
  "${PDAL_CARIS_SRC}/caris/caris_pc_wrapper.h"
)

set (PDAL_DRIVERS_CARIS_CPP
  "${PDAL_CARIS_SRC}/CloudReader.cpp"
  "${PDAL_CARIS_SRC}/pdal_csar.cpp"
  "${PDAL_CARIS_SRC}/Utils.cpp"
  "${PDAL_CARIS_SRC}/caris/caris_pc_wrapper.c"
)

if (CARIS_FOUND)
    list (APPEND PDAL_CPP ${PDAL_DRIVERS_CARIS_CPP} )
    list (APPEND PDAL_HPP ${PDAL_DRIVERS_CARIS_HPP} )
endif()


