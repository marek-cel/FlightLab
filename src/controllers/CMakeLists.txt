set(MODULE_NAME flightlab-controllers)

################################################################################

set(SOURCES
    PID/PID_controller.c
    PID/PID.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
