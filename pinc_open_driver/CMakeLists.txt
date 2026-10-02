cmake_minimum_required(VERSION 3.8)
project(pinc_open_driver)

# Dependencies
find_package(ament_cmake REQUIRED)
find_package(hardware_interface REQUIRED)
find_package(dynamixel_hardware_interface REQUIRED)

# Install
install(
  DIRECTORY launch meshes rviz urdf config
  DESTINATION share/${PROJECT_NAME}
)
install(PROGRAMS
  scripts/get_params
  scripts/pinc_open_driver_control_gui
  scripts/pinc_open_driver_monitor
  scripts/plot_pinc_open_driver_log
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()
