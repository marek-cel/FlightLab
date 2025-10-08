set(MODULE_NAME flightlab-actuators)

################################################################################

set(SOURCES
    actuators.c
    servo.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
