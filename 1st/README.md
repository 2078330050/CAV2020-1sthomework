秦天632004141518
=
一.安装VMware虚拟机
=
下载并安装VMware虚拟机软件并进行安装。[VMware官网](https://www.vmware.com/cn.html)

二.安装Ununtu 18.04
=
1.下载Ubuntu 18.04的镜像文件，并保存到本地磁盘上。[Ubuntu镜像下载](https://ubuntu.com/download/desktop)

2.打开VMware虚拟机软件，点击“新建虚拟机”，选择“典型（推荐）”并点击“下一步”。

3.在“选择安装媒体”界面，选择“使用ISO映像文件”，并选择之前下载好的Ubuntu 18.04的镜像文件，然后点击“下一步”。

4.在“选择操作系统”界面，选择“Linux”操作系统，并选择“Ubuntu 64位”版本，然后点击“下一步”。

5.在“命名虚拟机及选择存储位置”界面，输入虚拟机名称，并选择虚拟机存储位置，然后点击“下一步”。

6.在“指定磁盘容量”界面，选择虚拟机磁盘容量，并选择“将磁盘存储为单个文件”，然后点击“下一步”。

7.在“自定义硬件”界面，根据需要设置虚拟机的硬件配置，例如内存、CPU等，然后点击“完成”。

8.虚拟机创建完成后，点击“启动虚拟机”，进入Ubuntu 18.04的安装界面。

9.在Ubuntu 18.04的安装界面，选择语言、时区等基本信息，然后点击“继续”。

10.在“安装类型”界面，选择“其他选项”，然后点击“继续”。

11.在“磁盘分区”界面，选择“手动分区”，然后点击“继续”。

12.在“手动分区”界面，选择虚拟机磁盘，然后点击“新建分区”。

13.在“新建分区”界面，选择“逻辑分区”，设置分区大小、挂载点等信息，然后点击“确定”。

14.完成分区设置后，点击“安装现在”，开始安装Ubuntu 18.04系统。

15.安装完成后，重启虚拟机，进入Ubuntu 18.04系统。

16.打开终端，输入以下命令，更新软件源：

```sudo apt-get update```

三.安装ROS1
=
1.输入以下命令，安装ROS1：
--
```sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'```

```sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654```

```sudo apt-get update```

```sudo apt-get install ros-melodic-desktop-full```

2.输入以下命令，初始化ROS1：
--
```sudo rosdep init```

```rosdep update```

```echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc```

```source ~/.bashrc```

3.输入以下命令，创建ROS1工作空间：
--
```mkdir -p ~/catkin_ws/src```

```cd ~/catkin_ws/```

```catkin_make```

四.检查ROS1安装情况
=
运行小海龟

```roscore```

```rosrun turtlesim turtlesim_node```

```rosrun turtlesim turtle_teleop_key```

五.结果
=
！[VMware安装结果](https://github.com/2078330050/CAV2020-1sthomework/blob/main/mmexport1678771450632.png?raw=true)


！[Ubuntu 18.04安装结果](https://github.com/2078330050/CAV2020-1sthomework/blob/main/mmexport1678771452638.png?raw=true)

！[ROS1安装结果](https://github.com/2078330050/CAV2020-1sthomework/blob/main/1st/raw.githubusercontent.com_xiaowugui.png?raw=true)
