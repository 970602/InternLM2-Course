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
转化成Huggingface格式，也就是lora文件。
![1717053273629](https://github.com/970602/InternLM2-Course/assets/144504645/bb26abb0-2273-406b-b7b0-1e17c4221f5f)
# 模型整合
就是将训练出来的lora相当于一个adapter添加到原模型中，进行合并
![image](https://github.com/970602/InternLM2-Course/assets/144504645/54ff99c9-635c-46f5-b88a-5e5c0dea2bc7)

# 对话测试 
![image](https://github.com/970602/InternLM2-Course/assets/144504645/f6aac669-09ed-4aaf-8961-1a75695013e9)
过拟合
![image](https://github.com/970602/InternLM2-Course/assets/144504645/d78ef12f-e2ad-44c0-8d06-ae0d1c8adf21)
正常模型
![image](https://github.com/970602/InternLM2-Course/assets/144504645/b22e7a9c-ebba-4b17-ba1f-cf257c4f8c63)

# Web demo 部署
![image](https://github.com/970602/InternLM2-Course/assets/144504645/99b9453d-e43e-4f73-a649-5c73a093f79c)

## 进阶作业
![image](https://github.com/970602/InternLM2-Course/assets/144504645/2c50820f-7393-44dc-8dc0-381d3fd368ec)
## 复现多模态微调
# Finetune前
![image](https://github.com/970602/InternLM2-Course/assets/144504645/74006333-5c3c-4cba-b283-aa11a206c317)
# Finetune后
![image](https://github.com/970602/InternLM2-Course/assets/144504645/19ef50a4-dd04-4aae-80eb-75cf96bd8c3d)

