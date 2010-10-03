# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(luabitop C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
INCLUDE(dist.cmake)

ADD_LUA_MODULE(bit bit.c bit.def)

ADD_LUA_TEST(bittest.lua)
ADD_LUA_TEST(nsievebits.lua)
ADD_LUA_TEST(md5test.lua)

INSTALL (TARGETS bit DESTINATION ${INSTALL_CMOD})
INSTALL (DIRECTORY doc/ DESTINATION ${INSTALL_DOC})
INSTALL (FILES README DESTINATION ${INSTALL_DATA})
INSTALL (FILES bitbench.lua nsievebits.lua md5test.lua DESTINATION ${INSTALL_FOO})
INSTALL (FILES bittest.lua DESTINATION ${INSTALL_TEST})
