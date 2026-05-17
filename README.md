# GKD 开屏广告跳过规则

这是一个 GKD 订阅规则仓库，用于自动点击常见 App 开屏广告里的「跳过」「跳过广告」「Skip」按钮。

## 使用方式

1. 将仓库上传到 GitHub。
2. 在 GitHub 中打开 `gkd.json5`，点击 `Raw`。
3. 复制 Raw 链接，在 GKD 中添加为订阅。

上传后 Raw 链接通常是：

```text
https://raw.githubusercontent.com/<你的用户名>/<仓库名>/main/gkd.json5
```

## 文件说明

- `gkd.json5`：GKD 订阅规则。
- `gkd.version.json5`：轻量更新检测文件。

## 调整规则

如果某个 App 无法跳过广告，建议在 GKD 里抓取快照，再根据按钮节点补充更精确的应用规则。
