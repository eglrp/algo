project( Test3rdParty )

file( GLOB TEST_SRC_FILES *.cpp *.cc )
add_executable( ${PROJECT_NAME} ${TEST_SRC_FILES} )
target_link_libraries( ${PROJECT_NAME} ${CMAKE_THREAD_LIBS_INIT} 
    cppformat gmock )
set_target_properties( ${PROJECT_NAME} PROPERTIES FOLDER Tests )
install( TARGETS ${PROJECT_NAME} DESTINATION bin )
