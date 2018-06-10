cmake_minimum_required(VERSION 2.8)

project(bnf_plus_plus)

set( SOURCES
	src/bnf++gen.cc
	src/bnf++main.cc
	src/bnf++parser.cc )

add_executable( bnf_plus_plus ${SOURCES} )
target_include_directories( bnf_plus_plus PRIVATE src )
target_compile_options( bnf_plus_plus PRIVATE -DTEMPLATES_DIR="templates" -DPACKAGE_NAME="pkg" -DPACKAGE_VERSION="1" -include string.h )
