# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luacov NONE )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

install_lua_module ( luacov.defaults src/luacov/defaults.lua )
install_lua_module ( luacov src/luacov.lua )
install_lua_module ( luacov.reporter src/luacov/reporter.lua )
install_lua_module ( luacov.reporter.default src/luacov/reporter/default.lua )
install_lua_module ( luacov.runner src/luacov/runner.lua )
install_lua_module ( luacov.stats src/luacov/stats.lua )
install_lua_module ( luacov.tick src/luacov/tick.lua )
install_lua_module ( luacov.hook src/luacov/hook.lua )
install_lua_module ( luacov.util src/luacov/util.lua )

install_lua_executable ( luacov src/bin/luacov )

install_doc ( doc/ )
install_test ( tests/ )

install_data ( README.md )

