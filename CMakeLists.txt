
cmake_minimum_required (VERSION 2.8)
project (ProcessHollowing)

add_definitions(-DUNICODE -D_UNICODE)

set (srcs
	main.cpp
	pe_hdrs_helper.cpp
	sysutil.cpp
)

set (hdrs
	resource.h
	ntddk.h
	ntdll_undoc.h
	target_util.h
	createproc.h
	pe_hdrs_helper.h
	pe_raw_to_virtual.h
	relocate.h
	runpe.h
	sysutil.h
)

set (rsrc
	resource.rc
)

set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /SUBSYSTEM:WINDOWS /ENTRY:mainCRTStartup")

add_executable (ProcessHollowing ${rsrc} ${hdrs} ${srcs})

INSTALL( TARGETS ${PROJECT_NAME} DESTINATION ${CMAKE_INSTALL_PREFIX} COMPONENT ${PROJECT_NAME} )
