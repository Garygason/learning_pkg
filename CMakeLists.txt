cmake_minimum_required(VERSION 3.0.2)
project(learning_pkg)
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)


catkin_package(CATKIN_DEPENDS roscpp rospy std_msgs)

include_directories(${catkin_INCLUDE_DIRS})

# Add executables
add_executable(hello_cpp src/hello.cpp)
target_link_libraries(hello_cpp ${catkin_LIBRARIES})

add_executable(chatter src/chatter.cpp)
target_link_libraries(chatter ${catkin_LIBRARIES})

add_executable(listener src/listener.cpp)
target_link_libraries(listener ${catkin_LIBRARIES})


