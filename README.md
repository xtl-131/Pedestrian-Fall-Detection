# Pedestrian-Fall-Detection
基于Yolo系列模型的行人跌倒检测（三种方案）

### 环境配置(CPU版本,可自选，GPU可自行更改)：
```bash
conda create -n Fall python==3.9
conda activate Fall 
pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cpu
pip install -r requirements.txt
```

### 运行：
```bash
python detect.py
```
## 方案一：
基于Yolov8（也可以是其他版本的Yolo模型）的室内行人跌倒检测
该方案直接对行人进行检测并分类是否跌倒，数据集为自行收集整理，训练集7147张、验证集2112张
### demo

## 方案二：
基于Yolov8（也可以是其他版本的Yolo模型）和mediapipe的实时行人跌倒检测
该方案利用Yolo模型对people进行检测，而后将检测到人送入mediapipa进行关键点检测，最后通过计算相关骨骼节点之间的距离或者角度等来判断people是否跌倒
### demo

## 方案一：
基于Yolov8-pose（也可以是其他版本的Yolo模型）的实时行人跌倒检测
该方案利用Yolo-seg模型对people进行检测和关键点检测，而后通过计算相关骨骼节点之间的距离或者角度等来判断people是否跌倒
### demo

## 说明
三种方案均具备完整的数据集、跌倒检测界面系统，具体可加v:xtl-131或者q:1657092421
