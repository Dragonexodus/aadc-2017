set(CAR_TRAJECTORY htwk_car_trajectory)

set(CAR_TRAJECTORY_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR} PARENT_SCOPE)

if (TARGET ${CAR_TRAJECTORY})
    message("${CAR_TRAJECTORY} is already defined")
else ()
    file(GLOB_RECURSE FILES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
    file(GLOB_RECURSE HEADERS ${CMAKE_CURRENT_SOURCE_DIR}/*.h)

    ADD_LIBRARY(${CAR_TRAJECTORY} STATIC ${FILES} ${HEADERS})
endif ()
