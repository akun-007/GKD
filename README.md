# GKD 广告跳过规则

这是一个 GKD 订阅规则仓库，用于自动点击常见 App 广告里的「跳过」「跳过广告」「Skip」或关闭按钮。

## 添加订阅

在 GKD 中添加以下订阅链接：

```text
https://raw.githubusercontent.com/akun-007/GKD/main/gkd.json5
```

## 当前规则

- 通用规则：匹配常见开屏跳过按钮、倒计时跳过按钮与英文 `Skip` 按钮。
- 腾讯视频 `com.tencent.qqlive`：开屏广告跳过示例。
- 千鸟物联 `com.dayunlinks.cloudbirds`：进入首页后关闭右上角带叉号的小弹窗广告。

## 文件说明

- `gkd.json5`：GKD 订阅规则。
- `gkd.version.json5`：订阅更新检测文件。

## 提高匹配准确度

弹窗关闭按钮在不同 App 版本中可能使用不同控件。规则未生效或出现误触时，请在 GKD 中抓取弹窗出现时的快照，再根据按钮节点补充更精确的控件 `id`。
