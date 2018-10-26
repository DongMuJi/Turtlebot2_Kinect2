本文档对与TB2+Kinect2软件安装使用说明

1.参考教程安装kinect2本体驱动和Kinect2的ROS驱动,教程链接如下:
https://www.ncnynl.com/archives/201703/1439.html


2.安装Turtlebot的ROS包


3.将文件夹中的文件,放到相应的ROS包的文件夹下(一定要对应相应的路径)


4.连接TB2底座,连接Kinect2(一定要使用USB3.0)


5.输入环境变量, echo "export TURTLEBOT_3D_SENSOR=kinect2" >> ~/.bashrc && source ~/.bashrc


5.启动Turtlebot, roslaunch turtlebot_bringup minimal.launch


6.启动kinect2, roslaunch kinect2_bridge kinect2_laser.launch


7.gmapping+move_base, roslaunch turtlebot_navigation kinect2_gmapping.launch


8.map_serve+gmapping+move_base, roslaunch turtlebot_navigation kinect2_amcl.launch

