# 这是基于ChatGLM3的虚拟猫娘

![Demo webpage](assets/chat.png)

## 安装

我们建议通过 venv 进行环境管理。

执行以下命令新建一个 venv 环境并安装所需依赖：

PowerShell
```bash
python -m venv glm3-env
.\glm3-env\Scripts\Activate.ps1
pip install -r requirements.txt
```

请注意，本项目需要 Python 3.10 或更高版本。

## 运行

运行以下命令在本地加载模型并启动 demo：

```bash
streamlit run main.py
```

之后即可从命令行中看到 demo 的地址，点击即可访问。初次访问需要下载并加载模型，可能需要花费一定时间，因此建议提前下载好模型。

从此下载模型：(https://huggingface.co/THUDM/chatglm3-6b)

如果已经在本地下载了模型，可以通过 `export MODEL_PATH=/path/to/model` 来指定从本地加载模型

例如，这是完整的在PowerShell的运行命令：

```bash
F:\ChatGLM3\glm3-env\Scripts\Activate.ps1 ; $env:MODEL_PATH="G:\glm3" ; cd G:\cat_demo-for-ChatGLM3\ ; streamlit run main.py
```

模型默认多卡加载时自动切分模型

## 使用

- 用户可以直接在侧边栏修改 top_p, temperature, System Prompt 等参数来调整模型的行为

- 你可以根据你的需求来调整repetition_penalty的值。如果你希望生成的文本中有更多的变化，那么你可以将repetition_penalty设置为一个大于1.0的值。
  
    如果你不介意生成的文本中有一些重复的内容，那么你可以将repetition_penalty设置为1.0

    如果repetition_penalty等于1.0，那么模型将不会对重复的内容进行惩罚，这可能会导致生成的文本中出现大量的重复内容。
  
    如果repetition_penalty大于1.0，那么模型将会对重复的内容进行惩罚，这将减少生成的文本中的重复内容。repetition_penalty的值越大，对重复内容的惩罚就越大，因此生成的文本中的重复内容就越少。
  
    如果你可以接受生成的文本中有一些重复的内容，或者你希望模型更加倾向于人设中的内容，那么你可以将repetition_penalty设置为一个小于1.0的值。

- 然而，要注意的是，repetition_penalty并不直接控制文本的多样性。如果你想直接增加生成文本的多样性，你可能需要调整其他的参数，例如temperature或top_p。
  
    temperature参数可以控制生成文本的随机性，top_p参数可以控制在采样时，选择概率最高的前P个字符。这两个参数的值越高，生成的文本的多样性就越高。

### 额外技巧

- 在模型生成文本时，可以通过页面右上角的 `Stop` 按钮进行打断。
- 刷新页面即可清空对话记录。

# Enjoy!
