set(MODULE_NAME flightlab-aircrafts)

################################################################################

set(SOURCES
    boeing_737.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
