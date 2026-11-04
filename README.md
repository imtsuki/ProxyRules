# ProxyRules

飞书域名白名单，提供 Loon 规则集、Stash 规则集和 Stash 直连覆写。

## Stash iOS 安装

已有可用的 Stash 配置时，可以安装「飞书直连」覆写，让规则集中的域名走 `DIRECT`。

[一键安装飞书直连覆写](https://link.stash.ws/install-override/raw.githubusercontent.com/imtsuki/ProxyRules/main/Stash/Feishu.stoverride)

也可以在 Stash 的「覆写」页面选择「从 URL 下载 / Install from URL」，粘贴：

```text
https://raw.githubusercontent.com/imtsuki/ProxyRules/main/Stash/Feishu.stoverride
```

安装后启用覆写，并使用规则模式。覆写会合并规则集声明，将直连规则插入现有配置的规则前面；规则集每 24 小时更新。匹配范围以规则集中的域名为准，其中包含部分字节跳动共享域名。

## 规则集

- [Stash 域名规则集](https://raw.githubusercontent.com/imtsuki/ProxyRules/main/Stash/Feishu.yaml)：在 `rule-providers` 中使用，`behavior: domain`、`format: yaml`。
- [Loon 规则集](https://raw.githubusercontent.com/imtsuki/ProxyRules/main/Loon/Feishu.list)

规则集只包含匹配条件；Stash 覆写另外指定了 `DIRECT` 策略。

格式参考：[Stash 覆写](https://stash.wiki/configuration/override)、[规则集合](https://stash.wiki/rules/rule-set)、[一键安装链接](https://stash.wiki/faq/url-schema)。
