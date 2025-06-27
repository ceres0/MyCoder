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
