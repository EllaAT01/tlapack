# Copyright (c) 2025, University of Colorado Denver. All rights reserved.
#
# This file is part of <T>LAPACK.
# <T>LAPACK is free software: you can redistribute it and/or modify it under
# the terms of the BSD 3-Clause license. See the accompanying LICENSE file.

cmake_minimum_required(VERSION 3.5)

project( geqrtr CXX )

# Load <T>LAPACK
if( NOT TARGET tlapack )
  find_package( tlapack REQUIRED )
endif()

# add the example geqrtr
add_executable( example_geqrtr example_geqrtr.cpp )
target_link_libraries( example_geqrtr PRIVATE tlapack )
