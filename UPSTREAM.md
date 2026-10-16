# 来源与版本

- 原项目：https://github.com/shareAI-lab/learn-claude-code
- 固定版本：`ce8f9f186058939da54c9d6fead78dfb5d0fd6c3`
- 导入日期：2026-10-16（Asia/Shanghai）
- 许可证：MIT，见根目录 `LICENSE`，保留 `Copyright (c) 2024 shareAI Lab`。
- 本次导入：`s01_agent_loop/` 全部文件及上游 `requirements.txt`、`LICENSE`。
- `.env.example` 是为本课缩短的本地配置示例；`requirements.lock.txt` 是在 Windows / Python 3.13 上解析的固定依赖快照。
- 本仓库新增 README、中文学习教程与维护约定；上游 s01 源码保持原样。

## 官网与仓库的版本差异

检查时官网侧边栏列出 s01–s20，而上述源码提交的章节目录为 s01–s17。
二者从后续章节开始存在编号和主题差异；不能用数字直接认定为同一课。
官网 s01 的正文示例使用 `response.stop_reason`，本次固定的源码通过检查实际 `tool_use` 内容块决定是否继续。
本课以固定提交中的源码为可运行依据，以官网辅助理解。

后续课时先核对官网主题、上游代码路径和提交，再追加本仓库；不提前声称已有全部 20 课的对应源码。

原作者 README 中通往下一章节的相对链接，将在导入该章节后可用；现在可先查看上游仓库。
