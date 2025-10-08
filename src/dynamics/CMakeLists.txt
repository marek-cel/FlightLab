set(MODULE_NAME flightlab-dynamics)

################################################################################

set(SOURCES
    integrators/euler_integrator.c
    integrators/rk4.c
    aerodynamics.c
    eom.c
    forces.c
    gravity.c
    propulsion.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
