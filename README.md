# GPT-SoVITS

GPT-SoVITS是一个强大的语音合成工具，结合了GPT和SoVITS模型，可以实现高质量的语音合成。

## 必要模型下载

此仓库不包含预训练模型文件，请从以下链接下载所需模型：

### 必需模型
1. **BERT模型**：
   - 中文：[chinese-roberta-wwm-ext-large](https://huggingface.co/hfl/chinese-roberta-wwm-ext-large)
   - 放置路径：`GPT_SoVITS/pretrained_models/chinese-roberta-wwm-ext-large/`

2. **Hubert模型**：
   - 中文：[chinese-hubert-base](https://huggingface.co/TencentGameMate/chinese-hubert-base)
   - 放置路径：`GPT_SoVITS/pretrained_models/chinese-hubert-base/`

3. **SoVITS基础模型**：
   - 下载链接：[百度网盘](https://pan.baidu.com/s/1nrEVFGnx5CbPGKYHVjNmGg?pwd=5pyt) 提取码：5pyt
   - 文件：`s2G488k.pth` 和 `s1bert25hz-2kh-longer-epoch=68e-step=50232.ckpt`
   - 放置路径：`GPT_SoVITS/pretrained_models/`

### 可选工具模型
1. **分离人声模型**：
   - 下载链接：[百度网盘](https://pan.baidu.com/s/1nrEVFGnx5CbPGKYHVjNmGg?pwd=5pyt) 提取码：5pyt
   - 文件：`Bs_Roformer.pth` 和 `VR-DeEchoDeReverb.pth`
   - 放置路径：`tools/uvr5/uvr5_weights/`

2. **语音识别模型**：
   - 下载链接：[faster-whisper-large-v3](https://huggingface.co/Systran/faster-whisper-large-v3)
   - 放置路径：`tools/asr/models/faster-whisper-large-v3/`

## 使用方法

1. 下载上述所需模型文件并放置到对应目录
2. 安装依赖：`pip install -r requirements.txt`
3. 运行API服务：`python api.py -a 0.0.0.0 -p 9880`

## 阿里云函数计算部署说明

如需在阿里云函数计算上部署，请参考后面的Docker部署指南。 