# NCHU-NLP-Lab.AgriNER

考量文本亂碼之農業病蟲害領域命名實體識別研究

Google Colab：https://colab.research.google.com/drive/1WEfaSlKLLhNMVBnm68w4omWaWHVFg_U0?usp=sharing

## Requirements

This repo was tested on Python 3.6+ and PyTorch 1.5.1. The main requirements are:

- tqdm
- scikit-learn
- pytorch >= 1.5.1
- 🤗transformers == 2.2.2

To get the environment settled, run:

```
pip install -r requirements.txt
```

## Parameter Setting

### 1.model parameters

在./experiments/clue/config.json中設置了Bert/Roberta模型的基本參數，而在./pretrained_bert_models下的兩個預訓練文件夾中，config.json除了設置Bert/Roberta的基本參數外，還設置了'X'模型（如LSTM）參數，可根據需要進行更改。

### 2.other parameters

環境路徑以及其他超參數在./config.py中進行設置。

## Usage

打開指定模型對應的目錄，命令行輸入：

```
python run.py
```

模型運行結束後，最佳模型和訓練log保存在./experiments/clue/路徑下。在測試集中的bad case保存在./case/bad_case.txt中。
