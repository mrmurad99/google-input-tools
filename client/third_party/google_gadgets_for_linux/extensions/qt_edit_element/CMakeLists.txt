#
# Copyright 2008 Google Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

IF(GGL_BUILD_LIBGGADGET_QT)

APPLY_CONFIG(QT)

SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wno-conversion")

ADD_MODULE(qt-edit-element qt_edit_element.cc)
TARGET_LINK_LIBRARIES(qt-edit-element
  ggadget${GGL_EPOCH}
  ggadget-qt${GGL_EPOCH}
  ${QT_LIBRARIES}
)
OUTPUT_MODULE(qt-edit-element)

ENDIF(GGL_BUILD_LIBGGADGET_QT)
