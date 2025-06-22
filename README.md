# TrollAgent - iOS本地轻量化悬浮AI助手

![iOS悬浮AI界面]()  


TrollAgent是一款运行在iOS设备上的本地轻量化悬浮AI助手，使用先进的模型量化技术，可在设备端完全离线运行，提供智能对话和语言翻译服务。
支持15.-17.0 巨魔系统

## 🌟 功能特性

- **完全离线**：所有处理在设备端完成，无需联网
- **低资源占用**：优化内存/CPU使用，适合移动设备
- **多语言翻译**：支持英俄转中
- **悬浮交互**：便捷的悬浮窗口，随时随地使用
- **模型兼容**：支持通义千问(Qwen)全系列模型

## 🛠 技术栈

- **核心引擎**：[llama.cpp](https://github.com/ggerganov/llama.cpp) - 高性能大模型推理框架
- **语言模型**：Qwen系列GGUF格式量化模型
- **翻译模型**：`t5_translate_en_ru_zh`专用多语言模型
- **设备加速**：目前为适配低系统，未利用Metal框架实现GPU加速推理

---

### 🔍 模型下载链接

#### 语言模型
| 模型规格 | Hugging Face链接 | hf镜像(国内用户推荐) |
|---------|----------------|---------|
| **Qwen3-0.6BQ8** | [unsloth/Qwen3-0.6B-GGUF](https://huggingface.co/unsloth/Qwen3-0.6B-GGUF/tree/main) | [unsloth/Qwen3-0.6B-GGUF](https://hf-mirror.com/unsloth/Qwen3-0.6B-GGUF/tree/main) |
| **Qwen3-1.7B** | [unsloth/Qwen3-1.7B-GGUF](https://huggingface.co/unsloth/Qwen3-1.7B-GGUF/tree/main)| [unsloth/Qwen3-1.7B-GGUF](https://hf-mirror.com/unsloth/Qwen3-1.7B-GGUF/tree/main) |

#### 翻译模型
- **t5_translate_en_ru_zh**  
  *支持英语/俄语→中文的量化模型*
  | 模型规格 | Hugging Face链接 | hf镜像(国内用户推荐) |
  |---------|----------------|---------|
  | **small** | [PioneerMNDR/t5_translate_en_ru_zh_small_1024-Q8_0-GGUF](https://huggingface.co/PioneerMNDR/t5_translate_en_ru_zh_small_1024-Q8_0-GGUF/tree/main) | [PioneerMNDR/t5_translate_en_ru_zh_small_1024-Q8_0-GGUF](https://hf-mirror.com/PioneerMNDR/t5_translate_en_ru_zh_small_1024-Q8_0-GGUF/tree/main) |
  | **large** | [KeyserSoze1/t5_translate_en_ru_zh_large_1024_v2-Q8_0-GGUF](https://huggingface.co/KeyserSoze1/t5_translate_en_ru_zh_large_1024_v2-Q8_0-GGUF/tree/main) | [KeyserSoze1/t5_translate_en_ru_zh_large_1024_v2-Q8_0-GGUF](https://hf-mirror.com/KeyserSoze1/t5_translate_en_ru_zh_large_1024_v2-Q8_0-GGUF/tree/main) |
  
#### 模型的其他量化规格可以自行更换
---


## ⚙️ 模型配置
### 重命名并移动到指定位置
```bash
语言模型下载并放置 /var/mobile/TrollAgent/TrollAgent.gguf
翻译模型下载并放置 /var/mobile/TrollAgent/t5-translate.gguf
