# YourMoment ASMR 用户流程图

本目录包含 YourMoment ASMR 创作平台的 11 个用户流程泳道图（Mermaid 格式）。

## 文件列表

| 文件 | 说明 |
|------|------|
| [01-asmr-creation-flow.md](01-asmr-creation-flow.md) | 流程1：ASMR 创作完整流程（最详细） |
| [02-ai-text-asmr-flow.md](02-ai-text-asmr-flow.md) | 流程2：AI 文字生成 ASMR |
| [03-watch-asmr-flow.md](03-watch-asmr-flow.md) | 流程3：观看 ASMR 作品 |
| [04-register-login-flow.md](04-register-login-flow.md) | 流程4：用户注册登录 |
| [05-works-management-flow.md](05-works-management-flow.md) | 流程5：作品管理 |
| [06-community-flow.md](06-community-flow.md) | 流程6：社区浏览 |
| [07-collection-flow.md](07-collection-flow.md) | 流程7：收藏管理 |
| [08-settings-flow.md](08-settings-flow.md) | 流程8：用户设置 |
| [09-upload-failure-flow.md](09-upload-failure-flow.md) | 流程9：上传失败处理（异常） |
| [10-generation-failure-flow.md](10-generation-failure-flow.md) | 流程10：生成失败处理（异常） |
| [11-playback-failure-flow.md](11-playback-failure-flow.md) | 流程11：播放失败处理（异常） |

## 泳道说明

- **用户**：用户操作与输入
- **前端**：页面展示与请求
- **后端**：接口与业务逻辑
- **AI 服务**：仅流程1、2、10 涉及
- **数据库**：持久化存储

## 符号说明

- 圆角矩形 `([ ])`：开始 / 结束
- 矩形 `[ ]`：用户操作或系统处理
- 菱形 `{ }`：判断 / 决策
- 圆柱 `[( )]`：数据存储
- 实线箭头 `-->`：正常流向
- 虚线箭头 `-.->`：异常路径

## 导出为 PNG/JPG

1. **在线**：将各文件中的 Mermaid 代码块复制到 [Mermaid Live Editor](https://mermaid.live)，导出 PNG/SVG。
2. **命令行**：安装 `@mermaid-js/mermaid-cli` 后执行：
   ```bash
   npx @mermaid-js/mermaid-cli mmdc -i 01-asmr-creation-flow.md -o 01-asmr-creation-flow.png
   ```
   （若 .md 内含多处代码块，可先提取为单一 .mmd 再执行。）

## 异常流程与主流程关系

- 流程9：从流程1「上传」节点触发，处理后可回到流程1重新选择文件。
- 流程10：从流程1或流程2「生成」环节触发，用户可重试、重新上传/输入或取消。
- 流程11：从流程3「播放」环节触发，用户可重试、反馈或返回。
