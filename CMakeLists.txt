# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luabitop C )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

install_lua_module ( bit bit.c bit.def )

add_lua_test ( bittest.lua )
add_lua_test ( nsievebits.lua )
add_lua_test ( md5test.lua )

install_doc ( doc/ )
install_data ( README )
install_foo ( bitbench.lua nsievebits.lua md5test.lua )
install_test ( bittest.lua )
