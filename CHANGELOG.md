# Changelog

All notable changes to this project will be documented in this file.

## [5.5.13-papi-fix] - 2025-11-29
### English
- Fix: Avoid PlaceholderAPI async parsing crash on Folia servers by catching exceptions during placeholder parsing in `ComponentProvider`.
- Behaviour: If PAPI parsing fails for a placeholder, the original placeholder text will be left in place rather than causing the whole message to be dropped.
- Reason: Some PAPI expansions are not safe to call from async threads (Folia enforces stricter threading). Catching exceptions prevents message loss on first chat after join.
- Notes: Tested build artifact: `target/RedisChat-5.5.13-papi-fix.jar`.

### 中文 (Chinese)
- 修复：通过在 `ComponentProvider` 中捕获占位符解析异常，避免在 Folia 服务器上因 PlaceholderAPI 异步解析引发崩溃。
- 行为：如果 PAPI 解析某个占位符失败，会保留原始占位符文本，而不会导致整条消息丢失。
- 原因：部分 PAPI 扩展在异步线程中不安全（Folia 对线程模型更严格），捕获异常可防止玩家入服后第一条聊天丢失。
- 说明：已测试构建产物：`target/RedisChat-5.5.13-papi-fix.jar`。

---

Previous versions: see Git tags.