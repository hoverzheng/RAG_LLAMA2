# 通过ollama和streamlit，Chroma来构建RAG应用和专有知识库

## 说明
在之前源码的基础上进行了修改，使用ollama来管理大模型很方便，而且通过ollama提供的接口也很方便使用。


## Overview

检索增强引擎 (RAG) 是用于文档检索、摘要和交互式问答的强大工具。该项目利用 LangChain、Streamlit 和 Chroma 为用户提供无缝的 Web 应用程序来执行这些任务。使用 RAG，您可以轻松上传多个 PDF 文档，为这些文档中的文本生成矢量嵌入，并与文档执行对话交互。聊天历史记录也会被记住，以获得更具互动性的体验。

## 依赖库

- Python 3.7+
- LangChain
- Streamlit
- Ollama
- PDF documents to upload


## Usage

1. 将存储库克隆到本地：

   ```bash
   git clone https://github.com/wsxqaza12/RAG_LangChain_streamlit.git
   cd RAG_LangChain_streamlit
   ```

2. 通过运行以下命令安装所需的依赖项：
   ```bash
   pip install -r requirements.txt
   ```
   
3. 下载模型all-MiniLM-L6-v2到本地，若可以的话，也可以直接访问

4. 安装ollama，并通过ollama安装模型llama2-chinese大模型
   安装ollama大模型管理框架，并pull大模型：llama2-chinese。
   其中ollama服务，并在/etc/systemd/system/ollama.service文件种添加`Environment="OLLAMA_HOST=0.0.0.0:11434"`，这样可以远程访问。

3. Run the Streamlit app:
   ```bash
   streamlit run rag_engine.py
   ```

6. 上传想要分析的pdf文档

7. 点击"Submit Documents" 来处理pdf文档并生成vector embeddings.

9. 通过在聊天输入框中键入您的问题，与文档进行交互式对话。
