cmake_minimum_required (VERSION 2.8)
project (pe_unmapper)

add_definitions(-DUNICODE -D_UNICODE)
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} /MT")

set (srcs
	main.cpp
	pe_hdrs_helper.cpp
	pe_virtual_to_raw.cpp
	util.cpp
)

set (hdrs
	pe_hdrs_helper.h
	pe_virtual_to_raw.h
	relocate.h
	util.h
)

add_executable (pe_unmapper ${hdrs} ${srcs})
