# yue.nicholas@gmail.com

ADD_EXECUTABLE ( exrmultipart
  exrmultipart.cpp
)

TARGET_LINK_LIBRARIES ( exrmultipart
  IlmImf
  optimized Half                            debug Halfd
  optimized Iex${ILMBASE_LIBSUFFIX}         debug Iex${ILMBASE_LIBSUFFIX}d
  optimized IlmThread${ILMBASE_LIBSUFFIX}   debug IlmThread${ILMBASE_LIBSUFFIX}d
  ${PTHREAD_LIB}
  ${ZLIB_LIBRARIES}
)

INSTALL ( TARGETS
  exrmultipart
  DESTINATION
  ${CMAKE_INSTALL_PREFIX}/bin
)
