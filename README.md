## 依存関係

[TODO] 自動化
```
sudo apt install libudev-dev
```

## コンパイル

catkinでコンパイルする場合は、次のようにします。

```sh
catkin build

```

## rulesの追加

以下のコマンドを実行します。
```
sudo cp 99-lidar-ld06.rules /etc/udev/rules.d/
sudo service udev reload
```
その後、一度USBを指し直してください。


99-lidar-ld06.rules
```
SUBSYSTEM=="tty", ATTRS{idVendor}=="10c4", ATTRS{idProduct}=="ea60", SYMLINK+="ttyLD06"
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
