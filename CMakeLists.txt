cmake_minimum_required(VERSION 2.6)

include(cmake/base.cmake)

set(PROJECT_NAME ur5_description)
set(PROJECT_DESCRIPTION ur5 URDF model and meshes)
set(PROJECT_URL "")

setup_project()

install(DIRECTORY
  ${CMAKE_SOURCE_DIR}/urdf/
  DESTINATION ${CMAKE_INSTALL_DATADIR}/${PROJECT_NAME}/urdf
)

install(DIRECTORY
  ${CMAKE_SOURCE_DIR}/meshes/
  DESTINATION ${CMAKE_INSTALL_DATADIR}/${PROJECT_NAME}/meshes
)

setup_project_finalize()
