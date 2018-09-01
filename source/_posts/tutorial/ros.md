---
title: ROS
date: 2018-08-24 09:00:00
comments: true
tags:
     - ros 
categories: 
    - ros
---


Brief sum of ROS commands.

# official cheatsheet
[official cheatsheet pdf](https://github-production-release-asset-2e65be.s3.amazonaws.com/10255192/b1e25dbc-f7c3-11e4-9935-16b34cc459a0?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20180824%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20180824T134320Z&X-Amz-Expires=300&X-Amz-Signature=72769cb0ad90c933490684647a5415aee7b3be902d37589f835a5998ecfb0663&X-Amz-SignedHeaders=host&actor_id=9403813&response-content-disposition=attachment%3B%20filename%3DROScheatsheet_catkin.pdf&response-content-type=application%2Foctet-stream)

# installation
* <https://www.jianshu.com/p/68f88e377850>
* deal with ```segement fault``` when test```rqt rqt_graph rqt_graph```, solution https://blog.csdn.net/weixin_40047925/article/details/80263166.




# command table

command                   | meaning             
------------              | -------------
```rospack find [package_name]```               | get information about packages                
```roscd [locationname[/subdir]]```               |  to change directory (cd) directly to a package or a stack, also work for subdirectory e.g. ```roscd roscpp/cmake```                
```roscd log```   | take to ROS stores log files                
```rosls [locationname[/subdir]]```     | ls directly in a package by name
```Tab```     | Tab Completion
```catkin_create_pkg beginner_tutorials std_msgs rospy roscpp```     | create a new catkin package depend on std_mag etc
```catkin_make```     | build package
```rospack depends1/ depend ```     | check first-order/all dependency
```roscore```     | init
``` rosnode list ```     |  lists active nodes
``` rosnode info nodename ```     | information about a specific node
``` rosrun  [package_name] [node_name] ```     |  run a node within a package               
``` rosrun turtlesim turtlesim_node __name:=my_turtle ```     | rename a node               
``` rosnode ping```     | Test connectivity to node.                
``` rosrun rqt_graph rqt_graph```     | graph a topic               
```rostopic list -h```     | _              
``` rostopic type [topic]```     | e.g. ```rostopic type /turtle1/cmd_vel```                
``` rosmsg show msg ```             | e.g. ```rosmsg show geometry_msgs/Twist```                
``` rostopic pub [topic] [msg_type] [args]```     | e.g. ```rostopic pub -1 /turtle1/cmd_vel geometry_msgs/Twist -- '[2.0, 0.0, 0.0]' '[0.0, 0.0, 1.8]'```    
```rostopic hz [topic]```     | reports the rate at which data is published



# steps
## write and run python
1. cd under your package, e.g.              ```roscd beginner_tutorials/scripts/ ```    
2. edit python e.g.                  ```myCode.py```    
3. <span style="color:red"> make excutable</span>                    ```chmod +x listener.py```    
4. build like                   ```  cd ~/catkin_ws, catkin_make```      
5. start core                    ``` roscore```    ,
6. <span style="color:red"> source </span> setup.sh file,               ```  source ~/catkin_ws/devel/setup.bash```,
7. excute, e.g.         ```rosrun beginner_tutorials talker.py```.