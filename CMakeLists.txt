cmake_minimum_required ( VERSION 3.1 )
#########################################################################################
#
#   Library: Microsoft.Xna.Framework
#
#########################################################################################
project ( dark VERSION 0.1.0 )


list ( APPEND CSOURCE .lib/dark/src/Dark/Object.c )
list ( APPEND CSOURCE .lib/dark/src/Dark/Shape.c )
list ( APPEND CSOURCE .lib/dark/src/Dark/Rect.c )
list ( APPEND CSOURCE .lib/dark/src/Dark/Circle.c )

list ( APPEND VAPI .lib/dark/vapis/dark.vapi )

## Export to the parent scope:

set ( C_SOURCES "${C_SOURCES};${CSOURCE}" PARENT_SCOPE )
set ( INCLUDES "${INCLUDES}; ${CMAKE_SOURCE_DIR}/.lib/dark/include" PARENT_SCOPE )
set ( CUSTOM_VAPIS "${CUSTOM_VAPIS};${VAPI}" PARENT_SCOPE )
