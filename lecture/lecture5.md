# 第五节课作业（请交到第5节课）

## 基础作业（结营必做）
完成以下任务，并将实现过程记录截图：
- 配置 LMDeploy 运行环境
- 以命令行方式与 InternLM2-Chat-1.8B 模型对话

## 进阶作业

完成以下任务，并将实现过程记录截图：
- 设置KV Cache最大占用比例为0.4，开启W4A16量化，以命令行方式与模型对话。（优秀学员必做）
- 以API Server方式启动 lmdeploy，开启 W4A16量化，调整KV Cache的占用比例为0.4，分别使用命令行客户端与Gradio网页客户端与模型对话。（优秀学员必做）
- 使用W4A16量化，调整KV Cache的占用比例为0.4，使用Python代码集成的方式运行internlm2-chat-1.8b模型。（优秀学员必做）
- 使用 LMDeploy 运行视觉多模态大模型 llava gradio demo。（优秀学员必做）
- 将 LMDeploy Web Demo 部署到 [OpenXLab](../tools/openxlab-deploy/) 。


# InternStudio开发机创建conda环境
![image](https://github.com/970602/InternLM2-Course/assets/144504645/af79ce2c-a743-4085-8b07-d7701eb065bd)
# 使用Transformer库运行模型
![image](https://github.com/970602/InternLM2-Course/assets/144504645/d13ea5a7-9389-4e39-8bee-f8871f625934)
# 使用LMDeploy与模型对话
![image](https://github.com/970602/InternLM2-Course/assets/144504645/67654772-b580-4cd1-a091-ae203c781b07)
确实速度快非常多
# LMDeploy模型量化
#  查看默认情况下显存占比
![image](https://github.com/970602/InternLM2-Course/assets/144504645/215736e9-3d75-494a-8292-a338770d941a)
# 改变--cache-max-entry-count参数，设为0.5
![image](https://github.com/970602/InternLM2-Course/assets/144504645/a486fa66-ae76-4014-840a-f2d17065ff42)

# 把--cache-max-entry-count参数设置为0.01，约等于禁止KV Cache占用显存。
![image](https://github.com/970602/InternLM2-Course/assets/144504645/29dd4487-683f-42ae-974b-291d8f71fe81)

# 模型量化
# 使用Chat功能运行W4A16量化后的模型。
![image](https://github.com/970602/InternLM2-Course/assets/144504645/46868743-49f5-4f34-966a-b0d293ab0cce)
# 将KV Cache比例再次调为0.01，查看显存占用情况。
![image](https://github.com/970602/InternLM2-Course/assets/144504645/16aad920-cd93-4b9b-bd70-0f84163167d1)

## 设置KV Cache最大占用比例为0.4，开启W4A16量化，以命令行方式与模型对话
![image](https://github.com/970602/InternLM2-Course/assets/144504645/4213aaaa-08d5-43a8-8469-ca25cc4a630c)
##
# LMDeploy服务(serve)
![image](https://github.com/970602/InternLM2-Course/assets/144504645/5b00638f-e5cd-423b-b601-a87e8295e8cb)

## 以API Server方式启动 lmdeploy，开启 W4A16量化，调整KV Cache的占用比例为0.4
![image](https://github.com/970602/InternLM2-Course/assets/144504645/20ab6627-8c7f-446b-be2a-9389f4efaab2)

# 命令行客户端连接API服务器

![image](https://github.com/970602/InternLM2-Course/assets/144504645/c87bd947-cdd9-4e92-b896-e99e3129fb83)
# 网页客户端连接API服务器
![image](https://github.com/970602/InternLM2-Course/assets/144504645/f5224d80-e604-410c-b1ac-4274afe63969)
