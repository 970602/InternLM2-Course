# 第 4 节课作业

记录复现过程并截图

## 基础作业（结营必做）

- 训练自己的小助手认知（记录复现过程并截图）

## 进阶作业

- 将自我认知的模型上传到 OpenXLab，并将应用部署到 OpenXLab（优秀学员必做）
- 复现多模态微调（优秀学员必做）


OpenXLab 部署教程：https://github.com/InternLM/Tutorial/tree/camp2/tools/openxlab-deploy

## 基础作业
本地 clone 一个已有 pytorch 的环境
![image](https://github.com/970602/InternLM2-Course/assets/144504645/00145a81-6b2c-41bc-aecf-41dc71ed493d)
# 从源码安装 XTuner
![image](https://github.com/970602/InternLM2-Course/assets/144504645/3c8e0368-5af6-44cc-bc0d-47a8575f0561)
# 数据集准备

发现做微调的数据集是大量重复相同的指令。

![image](https://github.com/970602/InternLM2-Course/assets/144504645/a5a422dd-8992-4796-b80e-0f5a759271b8)
# 在 XTuner 已有的配置文件中，根据微调方法、数据集和模型挑选出最合适的配置文件并复制到我们新建的文件夹中
![image](https://github.com/970602/InternLM2-Course/assets/144504645/38c47590-d2d7-4f0d-aea4-0d2f805cd980)
# 修改配置文件
# 使用 deepspeed 来加速训练

出现错误。
![image](https://github.com/970602/InternLM2-Course/assets/144504645/ab9906f9-92ee-4ca3-a4e8-f3f6e7a8194b)
发现是版本问题，装v0.1.17  xtuner就行。

# 在微调后，如果echo过多，会发现过拟合的情况，也就是模型失去了基础的回答能力。一般有2种方法去处理。
  1. 设置一个保存权重的时间，去评估模型的效果
  2. 增加常规数据集，而来稀释特殊指令。比如10000条数据集中，添加20000条特殊指令。

# 模型转化
