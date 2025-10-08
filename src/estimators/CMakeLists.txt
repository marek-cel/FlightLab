set(MODULE_NAME flightlab-estimators)

################################################################################

set(SOURCES
    complementary_filter.c
    EKF.c
    simple_estimator.c
)

################################################################################

add_library(${MODULE_NAME} OBJECT ${SOURCES})
