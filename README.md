# ProxyRules

个人代理规则与 Stash 覆写。目前包含飞书域名白名单的 Loon、Stash 规则集，以及统一的个人 Stash 覆写。

## Stash iOS 安装

已有可用的 Stash 配置时，可以安装「个人覆写」。`Stash/Personal.stoverride` 是统一安装入口，后续分流规则及其他自定义设置都在这份文件中维护。目前启用的功能是飞书域名白名单直连。

[一键安装个人覆写](https://link.stash.ws/install-override/raw.githubusercontent.com/imtsuki/ProxyRules/main/Stash/Personal.stoverride)

也可以在 Stash 的「覆写」页面选择「从 URL 下载 / Install from URL」，粘贴：

```text
https://raw.githubusercontent.com/imtsuki/ProxyRules/main/Stash/Personal.stoverride
```

安装后启用覆写，并使用规则模式。后续更新个人设置时，在 Stash 中更新这份远程覆写即可。

当前覆写会合并飞书规则集声明，将直连规则插入现有配置的规则前面；飞书规则集每 24 小时更新。匹配范围以规则集中的域名为准，其中包含部分字节跳动共享域名。

如果此前安装了 `Feishu.stoverride`，请停用并删除旧覆写，改用上述个人覆写链接。

## 规则集

- [Stash 域名规则集](https://raw.githubusercontent.com/imtsuki/ProxyRules/main/Stash/Feishu.yaml)：在 `rule-providers` 中使用，`behavior: domain`、`format: yaml`。
- [Loon 规则集](https://raw.githubusercontent.com/imtsuki/ProxyRules/main/Loon/Feishu.list)

规则集只包含匹配条件，个人覆写集中维护这些规则集的策略及其他配置。

格式参考：[Stash 覆写](https://stash.wiki/configuration/override)、[规则集合](https://stash.wiki/rules/rule-set)、[一键安装链接](https://stash.wiki/faq/url-schema)。
