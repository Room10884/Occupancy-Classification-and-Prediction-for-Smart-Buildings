# 项目简介
当前很多建筑在无人时仍继续照明或空调，造成能源浪费。本项目使用智能传感器的实时数据（约每分钟采样一次），通过两类任务降低能源损耗：

1.基于当前时刻的五个特征（温度、湿度、光强、CO₂、时间戳衍生特征）做二分类：房间是否被占用（分类任务）。
2.基于过去 5–10 分钟的数据（滑窗），预测未来几分钟内房间是否会被占用（时序预测任务）。

# 使用的模型：

经典分类：Logistic Regression、Random Forest、XGBoost（暂定）
时序预测：LSTM、1D-CNN、基于滑窗特征的 XGBoost

# 数据集

### 数据来源：

https://archive.ics.uci.edu/dataset/357/occupancy+detection

### 本项目数据文件位于 dataset 文件夹：

../dataset/datatraining.txt
../dataset/datatest.txt
../dataset/datatest2.txt


### 文件包含以下传感器字段：

Date, Temperature, Humidity, Light, CO2, Occupancy (label)
