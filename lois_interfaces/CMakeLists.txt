cmake_minimum_required(VERSION 3.8)
project(lois_interfaces)

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/FilterOutput.msg"
  "msg/LoisGoal.msg"
  DEPENDENCIES std_msgs
  ADD_LINTER_TESTS
)

ament_package()
