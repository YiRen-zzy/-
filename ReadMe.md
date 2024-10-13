# 关于电控使用图传及串口的方法
## 远程连接NUC
+ 先在WiFi中连接‘RebornVision’ password：12345678
+ 打开终端
+ 输入`ssh reborn@192.168.31.248` password：1 (注意：这里的IP地址可能不同，具体询问视觉组)
## 图传
### 方案一
+ `git@github.com:YiRen-zzy/image_transport.git`
+ 在终端/编译器安装包
```bash
pip install opencv-python
pip install numpy
```
+ 运行python文件**image_sub.py**
### 方案二 (无需安装python)
+ 前往下载`https://mobaxterm.mobatek.net/`终端工具
+ 在该终端工具中远程连接NUC即可
+ 输入以下内容
```bash
cd image_transport/src/subcriber
python3 image_sub.py
```
## 串口通讯
+ 串口装在NUC上
+ 输入以下内容
```bash
cd Reborn-reborn-Intra-team-competition-demo
colcon build
source install /setup.bash
ros2 run example_topic topic_publisher
```
+ 在该终端内键盘输入操纵即可

