cmake_minimum_required(VERSION 3.8)
project(docking_action_server)

find_package(rclpy REQUIRED)
find_package(ament_cmake REQUIRED)
ament_python_install_package(commander)
find_package(rosidl_default_generators REQUIRED)

install(
  DIRECTORY commander
  DESTINATION share/${PROJECT_NAME}
)

rosidl_generate_interfaces(${PROJECT_NAME}
  "action/Docking.action"
)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  # the following line skips the linter which checks for copyrights
  # uncomment the line when a copyright and license is not present in all source files
  #set(ament_cmake_copyright_FOUND TRUE)
  # the following line skips cpplint (only works in a git repo)
  # uncomment the line when this package is not in a git repo
  #set(ament_cmake_cpplint_FOUND TRUE)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
