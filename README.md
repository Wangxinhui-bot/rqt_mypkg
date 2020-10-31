# 简单的rqt plugin例程
参考：https://wiki.ros.org/rqt/Tutorials

# 核心内容：
## UI界面
利用Qt Designer生成前段UI，放在resource中
## 回调函数
在src/my_module.py中链接回调函数和撰写回调函数

```
self._widget.pushButton.clicked.connect(self.on_pushButton_clicked)
```

```
    def on_pushButton_clicked(self):
```

# 其他内容
参考wiki，主要保证文件名一致即可，通过plugin.xml使其加入rqt中

# 订阅、发送消息，rosrun，roslaunch等操作
在my_module.py中，可以和ros节点一样，调用rospy即可subscribe和publish，唯一区别是不需要init node

对于roslaunch等需要，可以参考其API：http://wiki.ros.org/roslaunch/API%20Usage
