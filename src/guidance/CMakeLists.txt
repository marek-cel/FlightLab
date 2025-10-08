set(MODULE_NAME flightlab-guidance)

################################################################################

set(SOURCES
    guidance.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
