# 实验六 ROS Installation

## 1,Configure your Ubuntu repositories

	因为我的虚拟机可以联网，所以此步骤可以忽略

## 2,Setup your sources.list

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

## 3,Set up your keys

```
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
```

## 4,Installation

```
sudo apt-get update
```

​![pic1](http://ww4.sinaimg.cn/large/a16d1d95jw1f9l2bueauoj207g00iq2u.jpg)

```
sudo apt-get install ros-kinetic-desktop-full
```

​![pic2](http://ww3.sinaimg.cn/large/a16d1d95jw1f9l2dfevctj20k0054n04.jpg)

```
sudo apt-get install ros-kinetic-desktop
```

​![pic3](http://ww2.sinaimg.cn/large/a16d1d95jw1f9l2ec9uo8j20k105jdj1.jpg)

```
sudo apt-get install ros-kinetic-ros-base
```

​![pic4](http://ww4.sinaimg.cn/large/a16d1d95jw1f9l2f4an2bj20k105kgot.jpg)

```
sudo apt-get install ros-kinetic-slam-gmapping
```

​![pic5](http://ww2.sinaimg.cn/large/a16d1d95jw1f9l2fqxvz7j20jy054ad1.jpg)

## 5,Initialize rosdep

```
sudo rosdep init
rosdep update
```

​![pic6](http://ww1.sinaimg.cn/large/a16d1d95jw1f9l2h7oaglj20k209xgr1.jpg)

## 6,Environment setup

```
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

```
source /opt/ros/kinetic/setup.bash
```

## 7,Getting rosinstall

```
sudo apt-get install python-rosinstall
```

​![pic7](http://ww4.sinaimg.cn/large/a16d1d95jw1f9l2kmfwjjj20js04pjty.jpg)

