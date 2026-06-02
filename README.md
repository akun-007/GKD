# GKD 开屏广告跳过规则

这是一个 GKD 订阅规则仓库，用于自动点击常见 App 开屏广告里的「跳过」「跳过广告」「Skip」按钮。

## 添加订阅

在 GKD 中添加以下订阅链接：

```text
https://raw.githubusercontent.com/akun-007/GKD/main/gkd.json5
```

## 当前规则

- 通用规则：匹配常见跳过按钮、倒计时跳过按钮与英文 `Skip` 按钮。
- 应用专项示例：腾讯视频 `com.tencent.qqlive`。

## 文件说明

- `gkd.json5`：GKD 订阅规则。
- `gkd.version.json5`：订阅更新检测文件。

## 添加应用专项规则

如果某个 App 无法跳过广告，可以在 GKD 中抓取快照，根据按钮节点补充更精确的规则：

```json5
{
  id: '应用包名',
  name: '应用名称',
  groups: [
    {
      key: 0,
      name: '开屏广告',
      matchTime: 10000,
      actionMaximum: 1,
      resetMatch: 'app',
      rules: [
        {
          key: 0,
          matches: '[id="按钮控件 ID"][visibleToUser=true]',
        },
      ],
    },
  ],
}
```

建议优先使用控件 `id`，减少误触。
