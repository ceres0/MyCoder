# Vscode 系列

> 包含 VSCode、Cursor 等

## 问题

### Conda 环境运行 Python 代码遇到 9009 错误代码

> 参考 [VSCode使用code runner配置Anaconda环境](https://blog.csdn.net/accentd/article/details/142314305)

出现该问题主要是因为 Code Runner 插件默认配置有误

进入 Code Runner 插件的设置或在 VSCode 设置中搜索`@ext:formulahendry.code-runner`，找到 `Code-runner: Executor Map`，选择 `在 settings.json 中编辑`，然后将 Python 的执行命令修改为：

```json
"python": "set PYTHONIOENCODING=utf8 && $pythonPath -u $fullFileName",
```

## 插件

### Markdown Paste

#### 快捷键

- `Ctrl + Alt + v` 智能粘贴（图片、URL、HTML、富文本等）
- `Ctrl + Alt + d` 下载复制的链接并插入
- `Ctrl + Alt + c` 粘贴为代码格式
- `Ctrl + Alt + t` 对文字进行标注（如拼音等）
- `Ctrl + Alt + \` 插入 EMOJI或数学符号等

#### 开启 LLM AI 辅助

1. `MarkdownPaste.enableAI`设置为`true`
2. `MarkdownPaste.openaiConnectOption`中设置 LLM 的 apiKey
3. `MarkdownPaste.openaiCompletionTemplate`选择 model
