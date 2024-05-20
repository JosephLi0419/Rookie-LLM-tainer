# LLama Factory
提供很直觀的UI界面，並且提供超多種訓練模型的方法，最棒的是作者還有在更新！

### 硬體需求
![Screenshot from 2024-05-20 11-01-31](https://github.com/JosephLi0419/Rookie-LLM-trainer/assets/89914044/4c5afe2a-9407-4a25-a23c-28024ba2eea8)



### 需要的資料型態
- 資料前處理需要程式處理，可以參考我寫的這篇的思路：[LLM初探: 利用繁中語言模型打造臨床問診平台](https://medium.com/@evauni419/llm%E5%88%9D%E6%8E%A2-%E5%88%A9%E7%94%A8%E7%B9%81%E4%B8%AD%E8%AA%9E%E8%A8%80%E6%A8%A1%E5%9E%8B%E6%89%93%E9%80%A0%E8%87%A8%E5%BA%8A%E5%95%8F%E8%A8%BA%E5%B9%B3%E5%8F%B0-8c5e7449d072)

**alpaca**
```json
[
  {
    "instruction": "用户指令（必填）",
    "input": "用户输入（选填）",
    "output": "模型回答（必填）",
    "system": "系统提示词（选填）",
    "history": [
      ["第一轮指令（选填）", "第一轮回答（选填）"],
      ["第二轮指令（选填）", "第二轮回答（选填）"]
    ]
  }
]
```
**sharegpt**
```json
[
  {
    "conversations": [
      {
        "from": "human",
        "value": "用户指令"
      },
      {
        "from": "gpt",
        "value": "模型回答"
      }
    ],
    "system": "系统提示词（选填）",
    "tools": "工具描述（选填）"
  }
]
```
### 訓練方式
![Screenshot from 2024-05-20 11-12-06](https://github.com/JosephLi0419/Rookie-LLM-trainer/assets/89914044/b5ad8942-2a17-410c-a4c7-35538ed8e00e)

### 使用教學
```
git clone --depth 1 https://github.com/hiyouga/LLaMA-Factory.git ＃或者直接到github下載
cd LLaMA-Factory
conda create -n llama_factory-main python=3.10 #建立conda環境
conda activate llama_factory-main
pip install -e .[torch,metrics] ＃安裝需要的package
```
### 微調結果展示
- 正常的微調結果loss會在一開始向下，到一定程度後上下跳動
![image](https://github.com/JosephLi0419/Rookie-LLM-trainer/assets/89914044/f77b05b1-9f89-4fab-be4d-399b7bd30c14)