set(MODULE_NAME flightlab-sensors)

################################################################################

set(SOURCES
    aircraft_sensors.c
    altimeter.c
    gps.c
    imu.c
    magnetometer.c
    pitot_tube.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
