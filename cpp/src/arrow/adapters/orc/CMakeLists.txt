# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.

#######################################
# arrow_orc
#######################################

# Headers: top level
install(FILES
        adapter.h
        DESTINATION "${CMAKE_INSTALL_INCLUDEDIR}/arrow/adapters/orc")

# pkg-config support
configure_file(arrow-orc.pc.in
  "${CMAKE_CURRENT_BINARY_DIR}/arrow-orc.pc"
  @ONLY)
install(
  FILES "${CMAKE_CURRENT_BINARY_DIR}/arrow-orc.pc"
  DESTINATION "${CMAKE_INSTALL_LIBDIR}/pkgconfig/")
