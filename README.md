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

此外，使用 Code Interpreter 还需要安装 Jupyter 内核：

```bash
ipython kernel install --name chatglm3-demo --user
```

## 运行

运行以下命令在本地加载模型并启动 demo：

```bash
streamlit run main.py
```

之后即可从命令行中看到 demo 的地址，点击即可访问。初次访问需要下载并加载模型，可能需要花费一定时间。

如果已经在本地下载了模型，可以通过 `export MODEL_PATH=/path/to/model` 来指定从本地加载模型。如果需要自定义 Jupyter 内核，可以通过 `export IPYKERNEL=<kernel_name>` 来指定。

## 使用

### 对话模式

对话模式下，用户可以直接在侧边栏修改 top_p, temperature, System Prompt 等参数来调整模型的行为。例如


### 额外技巧

- 在模型生成文本时，可以通过页面右上角的 `Stop` 按钮进行打断。
- 刷新页面即可清空对话记录。

# Enjoy!
