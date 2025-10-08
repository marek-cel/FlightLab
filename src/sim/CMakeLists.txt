set(TARGET_NAME ${PROJECT_NAME})

################################################################################

set(SOURCES
    main.c
    scenarios.c
)

################################################################################

# add_library(${MODULE_NAME} OBJECT ${SOURCES})

add_executable(${TARGET_NAME} ${SOURCES})

set(LIBS m)

if(UNIX)
    set(LIBS
        ${LIBS}
    )
endif()

if(WIN32)
    set(LIBS
        ${LIBS}
    )
endif()

target_link_libraries(${TARGET_NAME}
    $<TARGET_OBJECTS:flightlab-actuators>
    $<TARGET_OBJECTS:flightlab-aircrafts>
    $<TARGET_OBJECTS:flightlab-controllers>
    $<TARGET_OBJECTS:flightlab-core>
    $<TARGET_OBJECTS:flightlab-dynamics>
    $<TARGET_OBJECTS:flightlab-estimators>
    $<TARGET_OBJECTS:flightlab-guidance>
    $<TARGET_OBJECTS:flightlab-io>
    $<TARGET_OBJECTS:flightlab-math>
    $<TARGET_OBJECTS:flightlab-sensors>
    ${LIBS}
)


