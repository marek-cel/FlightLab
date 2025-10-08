set(MODULE_NAME flightlab-core)

################################################################################

set(SOURCES
    constants.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
