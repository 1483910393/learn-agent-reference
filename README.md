# Learn Agent：逐课参考实现

跟随 [Learn Claude Code](https://learn.shareai.run/zh/s01/) 学习 Agent Harness。
本仓库由助手按课时维护，当前只加入 **s01 Agent Loop**。

源码来自 [shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)，保留原作者 MIT 许可证；不是助手原创代码。`s01_agent_loop/` 保留上游文件原文，讲解单独放在 `docs/`。

## 两条学习线

| 仓库 | 可见性 | 约定 |
| --- | --- | --- |
| [learn-agent-reference](https://github.com/1483910393/learn-agent-reference) | 公开 | 助手导入、验证并逐课维护参考源码 |
| learn-agent-practice | 私有 | 学生自己敲代码、配置环境、提交与上传；助手提供解释和排错 |

## 从这里开始

1. 阅读 [第一课：配置环境与首次上传](docs/s01-第一课.md)。
2. 按 [第一课：分块手敲源码](docs/s01-分块手敲.md) 完成自己的实现。
3. 参考 [原作者中文讲解](s01_agent_loop/README.zh.md) 和 [未经改写的源码](s01_agent_loop/code.py)。
4. 查看 [来源与版本](UPSTREAM.md)、[维护约定](docs/维护约定.md)。

## Windows PowerShell 快速运行

```powershell
uv venv --python 3.13 .venv
uv pip install --python .venv/Scripts/python.exe -r requirements.lock.txt
Copy-Item .env.example .env
# 在本机编辑 .env，填入真实的 ANTHROPIC_API_KEY。
New-Item -ItemType Directory -Path sandbox -Force
Set-Location sandbox
..\.venv\Scripts\python.exe ..\s01_agent_loop\code.py
```

在 `sandbox` 目录运行，使模型操作从练习目录开始。此目录只是工作目录，**不是权限隔离沙箱**；s01 的简单命令拒绝列表也不是完整安全机制。第一课先做列目录、写 `hello.py` 这类小练习。

本课程调用付费模型 API；Claude / ChatGPT 聊天订阅和 API 计费分开。模型名称沿用导入时上游示例，实际可用性以自己的 Anthropic 控制台为准。

## 当前验证状态

本机环境、依赖安装、无网络的循环行为检查和 GitHub 上传结果见本机学习档案。真实 API 调用等待学生在本地填写密钥后亲自完成。
