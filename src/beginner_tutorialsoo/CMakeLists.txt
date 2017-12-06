# %Tag(FULLTEXT)%
cmake_minimum_required(VERSION 2.8.3)
project(beginner_tutorialsoo)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS 
roscpp 
rospy
std_msgs 
genmsg
message_generation)

## Declare ROS messages and services
#add_message_files(DIRECTORY msg FILES Num.msg)
add_service_files(FILES AddTwoInts.srv)
## Generate added messages and services
generate_messages(DEPENDENCIES std_msgs)

## Declare a catkin package
catkin_package()
include_directories(${catkin_INCLUDE_DIRS})

add_executable(beginner_tutorialsoo src/add_two_ints_server.cpp)
target_link_libraries(beginner_tutorialsoo ${catkin_LIBRARIES})
add_dependencies(beginner_tutorialsoo beginner_tutorialsoo_generate_messages_cpp)

# %EndTag(FULLTEXT)%
