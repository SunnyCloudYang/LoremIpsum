# 中文假字生成器

[![Website chinese-lorem-ipsum.vercel.app](https://img.shields.io/website-up-down-green-red/https/naereen.github.io.svg)](https://chinese-lorem-ipsum.vercel.app/) [![GitHub license](https://badgen.net/github/license/Naereen/Strapdown.js)](https://github.com/SunnyCloudYang/Chinese-lorem-ipsum/blob/main/LICENSE) [![API](https://img.shields.io/badge/API-Free-darkgreen)](https://github.com/SunnyCloudYang/Chinese-lorem-ipsum/blob/main/website/api/apidoc.md)

## 描述

该项目基于**真实世界的中文字符频率**生成随机文本（乱数假文）。它从现代汉语语料库词频表中读取词语频率，并按照词频生成随机句子。

默认情况下，它会生成包含 3\~5 段，每段 4\~8 句，每句不超过20个字的随机文本，大约300字。

但是你可以通过传递不同的参数轻松自定义段落数、每段句子数和每句字数。此外还可以生成指定字数的随机文本。

## 网站

[中文假字生成器](https://chinese-lorem-ipsum.vercel.app/)

## API

[API 文档](https://github.com/SunnyCloudYang/Chinese-lorem-ipsum/blob/main/website/api/apidoc.md)

## 项目结构

```plaintext
Chinese-lorem-ipsum/
├── website/                  # 网站
│   ├── api/                  # 后端 API
│   │   ├── apidoc.md         # API 文档
│   │   └── app.py            # flask app
│   ├── index.html            # 主页
│   └── ...                   # 其他网站文件
├── data/                     # 数据源
│   ├── word_freq.txt         # 词频表（预处理时生成）
│   ├── char_freq.txt         # 字频表（预处理时生成）
│   ├── 现代汉语语料库词频表    # 词频表
│   └── 现代汉语语料库字频表    # 字频表
├── train/                    # 使用了Markov模型的测试版本
│   ├── clean_corpus.py       # 清理语料库的脚本
│   └── model.py              # Markov模型
├── model/                    # Markov模型文件
│   └── model.json            # Markov模型
├── lorem_ipsum.py            # 生成随机文本的脚本
├── preprocess.py             # 预处理词频表的脚本
└── ...                       # 其他文件
```

## 安装

### 本地安装

1. 克隆仓库：

    ```sh
    git clone https://github.com/SunnyCloudYang/Chinese-lorem-ipsum.git
    ```

2. 进入项目目录：

    ```sh
    cd Chinese-lorem-ipsum
    ```

3. 设置虚拟环境：

    ```sh
    python -m venv venv
    ```

4. 激活虚拟环境：
    - 在 Windows 上：

        ```sh
        venv\Scripts\activate
        ```

    - 在 macOS/Linux 上：

        ```sh
        source venv/bin/activate
        ```

5. 安装依赖：

    ```sh
    pip install -r requirements.txt
    ```

### 网站安装

1. 克隆仓库：

    ```sh
    git clone https://github.com/SunnyCloudYang/Chinese-lorem-ipsum.git
    ```

2. 进入项目目录：

    ```sh
    cd Chinese-lorem-ipsum/website
    ```

3. 安装依赖：

    ```sh
    npm install
    ```

## 使用

### 交互式

1. 进入网站目录：

    ```sh
    cd Chinese-lorem-ipsum/website
    ```

2. 运行 Vercel 开发服务器：

    ```sh
    vercel dev
    ```

3. 打开浏览器并导航到 [`http://localhost:3000`](http://localhost:3000)。
4. 点击“生成”按钮生成随机文本。

### 脚本

1. 确保项目目录中有 `word_freq.txt`文件。
2. 运行脚本生成包含 3\~5 段，每段 4\~8 句的随机文本：

    ```sh
    python lorem_ipsum.py
    ```

## 贡献

1. Fork 仓库。
2. 创建新分支：

    ```sh
    git checkout -b feature/your-feature
    ```

3. 进行更改并提交：

    ```sh
    git commit -m "Add your message"
    ```

4. 推送到分支：

    ```sh
    git push origin feature/your-feature
    ```

5. 提交 pull request。

## 许可证

该项目使用 MIT 许可证。

## 联系

[sunnycloudyang@outlook.com](mailto:sunnycloudyang@outlook.com)
