# AI 助手项目

本项目是一个通过快捷键调用不同AI模型进行对话的Python脚本，支持多种AI模型和TTS（文本转语音）功能。

## 功能特性

- 支持多种AI模型：Gemini、Qwen、QWQ、Grok、Baidu、Zhipu、Aliyun等
- 提供TTS功能，支持流式和非流式两种模式
- 通过快捷键快速调用不同模型
- 支持取消当前对话和退出程序

## 安装依赖

```bash
pip install -r requirements.txt
```

## 使用方法

1. 运行主脚本：
   ```bash
   python ai_assistant/ai_assistant.py
   ```

2. 使用快捷键调用不同功能：

   | 快捷键       | 功能描述               |
   |--------------|------------------------|
   | f9+o         | 调用OpenAI模型         |
   | f9+g         | 调用Gemini模型         |
   | f9+x         | 调用Grok模型           |
   | f9+q         | 调用Qwen模型           |
   | f9+w         | 调用QWQ模型            |
   | f9+b         | 调用Baidu模型          |
   | f9+z         | 调用Zhipu模型          |
   | f9+a         | 调用Aliyun模型         |
   | f9+l         | 调用Aliyun Web模型     |
   | f9+1         | 调用TTS                |
   | esc+1        | 停止TTS                |
   | f9+2         | 调用流式TTS            |
   | f9+3         | 调用非流式TTS          |
   | esc          | 取消当前对话           |
   | esc+f9       | 退出程序               |

## 项目结构

```
ai_assistant/
├── ai_assistant/
│   ├── assistant/                # 子模块目录
│   │   ├── __init__.py           # 包初始化文件
│   │   ├── base.py               # 基础类定义
│   │   ├── openai_model.py       # OpenAI模型实现
│   │   ├── qwen_model.py         # 通义千问模型实现
│   │   ├── qwq_model.py          # QWQ模型实现
│   │   ├── chat_with_tts_no_stream.py  # 非流式TTS对话实现
│   │   ├── chat_with_tts_stream.py     # 流式TTS对话实现
│   │   ├── openai_tts.py         # OpenAI TTS实现
│   │   ├── tts_client.py         # TTS客户端实现
│   │   └── tts_server.py         # TTS服务器实现
│   ├── __init__.py               # 包初始化文件
│   └── ai_assistant.py           # 主程序脚本
├── README.md                     # 项目说明文件
├── requirements.txt              # 项目依赖文件
└── pyproject.toml                # 项目配置文件

## 贡献指南

欢迎提交Pull Request或Issue来改进本项目。

## 许可证

MIT License