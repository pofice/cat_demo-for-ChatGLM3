# 这是基于ChatGLM3的虚拟猫娘

![Demo webpage](assets/chat.png)

## 安装

我们建议通过 venv 进行环境管理。

执行以下命令新建一个 venv 环境并安装所需依赖：

```bash
python -m venv glm3-env
cd glm3-env
.\glm3-env\Scripts\Activate.ps1
pip install -r requirements.txt
```

请注意，本项目需要 Python 3.10 或更高版本。

## 运行

运行以下命令在本地加载模型并启动 demo：

```bash
streamlit run main.py
```

之后即可从命令行中看到 demo 的地址，点击即可访问。初次访问需要下载并加载模型，可能需要花费一定时间。

如果已经在本地下载了模型，可以通过 `export MODEL_PATH=/path/to/model` 来指定从本地加载模型

例如，这是完整的在powershell的运行命令：

```bash
F:\ChatGLM3\glm3-env\Scripts\Activate.ps1 ; $env:MODEL_PATH="G:\glm3" ; cd G:\cat_demo-for-ChatGLM3\ ; streamlit run main.py
```
## 使用

用户可以直接在侧边栏修改 top_p, temperature, System Prompt 等参数来调整模型的行为

你可以根据你的需求来调整repetition_penalty的值。如果你希望生成的文本中有更多的变化，那么你可以将repetition_penalty设置为一个大于1.0的值。如果你不介意生成的文本中有一些重复的内容，那么你可以将repetition_penalty设置为1.0

### 额外技巧

- 在模型生成文本时，可以通过页面右上角的 `Stop` 按钮进行打断。
- 刷新页面即可清空对话记录。

# Enjoy!
