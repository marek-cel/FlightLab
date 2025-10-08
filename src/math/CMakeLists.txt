set(MODULE_NAME flightlab-math)

################################################################################

set(SOURCES
    dcm.c
    matrix.c
    quat.c
    utils.c
    vector.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
