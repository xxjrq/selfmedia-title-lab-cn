# 自媒体标题改写

免费、免第三方 API Key 的中文标题改写 Skill。它复用你给出的正文事实，为抖音、小红书、B站各写 3 条差异化标题，再挑出最贴合正文的一条；不承诺爆款，也不把任务扩展成视频制作或发布流程。

## 立即使用

把下面的内容交给支持 Skill 的助手即可：

```yaml
核心收益: 用手机现有照片做出干净的商品主图，减少反复拍摄
正文: |
  这篇内容演示用手机相册的裁切、亮度和白平衡功能，整理一张白色马克杯的照片。
  重点是保留杯身细节、统一背景亮度，再导出 1:1 图片。没有使用付费软件，也不涉及拍摄教学。
平台: [抖音, 小红书, B站]
```

你会得到类似仓库中 [成功样例](fixtures/success-output.md) 的可复制标题清单和一条推荐。缺少“核心收益”、正文或平台时，Skill 会像 [失败样例](fixtures/failure-expected.md) 一样指出缺项，而不会杜撰内容。

## 使用范围

- 适合中文自媒体创作者和小店经营者。
- 输入只需核心收益、正文与平台；可补充目标受众、语气或限制词。
- 只输出标题与简短推荐理由；所有标题以输入中的可验证事实为边界。
- 不需要浏览器、账号或外部服务，因此不采集登录态，也不会操作发布平台。

## 安装与校验

将本目录作为独立 Skill 安装后，按 `SKILL.md` 的输入格式使用。仓库自检不生成标题，只验证真实的结构和成功/失败样例：

```bash
node scripts/self-test.mjs
node ../skill-seo/scripts/audit.mjs --root . --output /tmp/selfmedia-title-lab-cn-seo --strict
```

## 来源与原创性

本 Skill 的标题工作流、文案和代码均为原创实现。仅核对以下公开项目的业务用途和许可证，不复制其源码或文档；2026-10-04 核对时，`marketingskills` 与 `easy-webbridge` 的仓库许可证均为 MIT，`anthropics/skills` 的 GitHub 许可证接口未返回已识别许可证：

- [marketingskills](https://github.com/coreyhaines31/marketingskills)（业务类 Skill 的公开发布参考）
- [anthropics/skills](https://github.com/anthropics/skills)（Skill 组织方式参考）
- [Easy WebBridge](https://github.com/xxjrq/easy-webbridge)（浏览器隔离能力参考；本 Skill 不需要浏览器）

许可证见 [LICENSE](LICENSE)。
