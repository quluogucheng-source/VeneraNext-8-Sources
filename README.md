# VeneraNext-8-Sources

为 VeneraNext 定制的 8 源漫画源仓库。

- 数据来源：官方仓库 `venera-app/venera-configs`（main 分支），脚本文件为官方原文件，逐字节一致，未做任何修改。
- 索引格式：与官方 `index.json` 完全一致（`name` / `fileName` / `key` / `version`），符合 VeneraNext 源仓库导入协议。
- 不包含任何其他漫画源。

## 收录的 8 个漫画源

| 名称 | 脚本文件 | key | 版本 |
| --- | --- | --- | --- |
| Komiic | komiic.js | Komiic | 1.0.3 |
| 拷贝漫画 | copy_manga.js | copy_manga | 1.4.3 |
| 拷贝漫画(多账号) | copy_manga_multi_accounts.js | copy_manga_multi_accounts | 1.4.1 |
| GoDa漫画 | goda.js | goda | 1.2.1 |
| 漫画人 | manhuaren.js | manhuaren | 1.0.0 |
| 漫画柜 | manhuagui.js | ManHuaGui | 1.2.1 |
| CCC追漫台 | ccc.js | ccc | 1.0.1 |
| 再漫画 | zaimanhua.js | zaimanhua | 1.0.2 |

> 注：用户侧所称「拷贝漫画 M（多账号版）」对应官方索引中的「拷贝漫画(多账号)」，key 为 `copy_manga_multi_accounts`，与「拷贝漫画」是两个独立条目，均可独立安装。

## 在 VeneraNext 中添加（一个网址导入 8 源）

1. 打开 VeneraNext →「漫画源」→「添加来源」。
2. 粘贴下方列表地址（推荐 jsDelivr 地址，中国大陆访问更稳定）：

   ```
   https://cdn.jsdelivr.net/gh/<你的GitHub用户名>/VeneraNext-8-Sources@main/index.json
   ```

3. 点击「识别并预览」：应显示 8 个可安装条目、0 个无效条目。
4. 全选后点击「安装所选」（也可勾选「保存为来源仓库」以便日后检查更新）。
5. 返回「已安装」确认 8 个源全部安装成功。

备用地址（GitHub Raw，网络不佳时可能超时）：

```
https://raw.githubusercontent.com/<你的GitHub用户名>/VeneraNext-8-Sources/main/index.json
```

## 结构

```
index.json                     # 源索引（JSON 数组，8 条）
komiic.js                      # 官方原文件
copy_manga.js
copy_manga_multi_accounts.js
goda.js
manhuagui.js
manhuaren.js
ccc.js
zaimanhua.js
README.md
CHECK.md                       # 构建与验证报告
```

## 版权说明

- 本仓库中的 `.js` 文件为 `venera-app/venera-configs`（官方配置仓库）的原文件镜像，未经修改，仅作转发/分发使用；官方仓库未声明 LICENSE，使用时请自行评估。
- 索引数据（名称、版本号）取自官方 `index.json`，未自行编造或改写。
- 漫画源的实际内容与可用性取决于源站与官方扩展实现，与本仓库无关。
