# TrollAgent - iOS本地轻量化悬浮AI助手

![iOS悬浮AI界面]()  


TrollAgent是一款运行在iOS设备上的本地轻量化悬浮AI助手，使用先进的模型量化技术，可在设备端完全离线运行，提供智能对话和语言翻译服务。

## 🌟 功能特性

- **完全离线**：所有处理在设备端完成，无需联网
- **低资源占用**：优化内存/CPU使用，适合移动设备
- **多语言翻译**：支持英俄转中
- **悬浮交互**：便捷的悬浮窗口，随时随地使用
- **模型兼容**：支持通义千问(Qwen)全系列模型

## 🛠 技术栈

- **核心引擎**：[llama.cpp](https://github.com/ggerganov/llama.cpp) - 高性能大模型推理框架
- **语言模型**：[Qwen系列GGUF格式量化模型](https://hf-mirror.com/unsloth/Qwen3-0.6B-GGUF/blob/main/Qwen3-0.6B-Q8_0.gguf)
- **翻译模型**：[`t5_translate_en_ru_zh`专用多语言模型](https://hf-mirror.com/iG8R/t5_translate_en_ru_zh_large_1024_v2-Q8_0-GGUF/blob/main/t5_translate_en_ru_zh_large_1024_v2-q8_0.gguf)
- **设备加速**：目前为适配低系统，未利用Metal框架实现GPU加速推理


## ⚙️ 模型配置
### 重命名并移动到指定位置
```bash
mv ~/Downloads/qwen_model.gguf /var/mobile/TrollAgent/TrollAgent.gguf
mv ~/Downloads/t5.gguf /var/mobile/TrollAgent/t5-translate.gguf
