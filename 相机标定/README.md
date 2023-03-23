一、准备工作
=

1、启动ros
--
```roscore```

2、启动usb_cam
--
```roslaunch usb_cam usb_cam-test.launch```

出现图像![启动camera](https://github.com/2078330050/CAV2020-1sthomework/blob/main/%E7%9B%B8%E6%9C%BA%E6%A0%87%E5%AE%9A/%E5%90%AF%E5%8A%A8camera.png?raw=true)

3、配置ROS的相机标定包
--
```sudo apt-get install ros-melodic-camera-calibration```

4、打印棋盘格
--
[A4-7x5-26棋盘格](https://github.com/2078330050/CAV2020-1sthomework/blob/main/%E7%9B%B8%E6%9C%BA%E6%A0%87%E5%AE%9A/calib.io_checker_210x297_6x4_26.pdf)

二、开始标定
=

1、启动相机
--
```roslaunch usb_cam usb_cam-test.launch```

2、启动标定程序
--
```rosrun camera_calibration cameracalibrator.py --size 4x6 --square 0.026 image:=/usb_cam/image_raw camera:=/usb_cam```

X：表示标定板在视野中的左右位置

Y：表示标定板在视野中的上下位置

Size：表示标定板在视野中的尺寸大小，其实就是离相机的远近

Skew：表示标定板在视野中的倾斜角度

3、开始标定
--
调整标定板的位置，让它在相机视野中各个位置移动和转动，让X、Y、Size和Skew这四个值下面的长条变成绿色，然后CALIBRATE这个按钮会变成青色，点击CALIBRATE开始计算相机的参数。

计算完成后SAVE按钮会变成青色，点击SAVE按钮把数据保存到默认的目录/tmp/calibrationdata.tar.gz下。

三、标定结果
=
[ost.txt](https://github.com/2078330050/CAV2020-1sthomework/blob/main/%E7%9B%B8%E6%9C%BA%E6%A0%87%E5%AE%9A/ost.txt)

[ost.yaml](https://github.com/2078330050/CAV2020-1sthomework/blob/main/%E7%9B%B8%E6%9C%BA%E6%A0%87%E5%AE%9A/ost.yaml)
