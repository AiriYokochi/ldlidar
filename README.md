## コンパイル

catkinでコンパイルする場合は、次のようにします。

```sh
catkin_make

```



## 実行方法

```sh
source devel/setup.bash
roslaunch ldlidar ld06.launch 

or

rosrun ldlidar ldlidar 
```



## テスト

Ubuntu16.04 kinetic versionでテストされ、rvizを使用して可視化します。
