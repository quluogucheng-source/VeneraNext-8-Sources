# CHECK — 构建与验证报告

生成时间：2026-11-02 16:16:01（本地）
数据来源：https://github.com/venera-app/venera-configs （分支 main）
索引字段交叉核对：与官方 index.json 逐字段比对（name/fileName/key/version）

## 1. 索引校验

- JSON 可解析：通过（UTF-8 无 BOM，bytes=1091）
- 条目数量：8（要求恰好 8）
- key 唯一：通过
- key 正则 ^\w+$：全部通过
- version 正则 ^\d+\.\d+\.\d+(?:[.\-].+)?$：全部通过
- 与官方索引字段一致性：全部通过（无编造文件名/版本号）

## 2. 脚本文件字节级校验（本地镜像 vs 官方 jsDelivr）

| key | 文件名 | 本地大小 | sha256(本地) | sha256(jsDelivr官方) | 一致性 |
| --- | --- | --- | --- | --- | --- |
| Komiic | komiic.js | 23269 B | a467325b6be833af… | a467325b6be833af… | 通过 |
| copy_manga | copy_manga.js | 39835 B | 5012ce0782dc0410… | 5012ce0782dc0410… | 通过 |
| copy_manga_multi_accounts | copy_manga_multi_accounts.js | 51907 B | 1d8d8f855fed67ab… | 1d8d8f855fed67ab… | 通过 |
| goda | goda.js | 16366 B | dc94b8d5074e3426… | dc94b8d5074e3426… | 通过 |
| manhuaren | manhuaren.js | 39376 B | 6ec9b7ca3f843698… | 6ec9b7ca3f843698… | 通过 |
| ManHuaGui | manhuagui.js | 47555 B | a5bf6c633e0ce728… | a5bf6c633e0ce728… | 通过 |
| ccc | ccc.js | 31878 B | d7db634cd6a66782… | d7db634cd6a66782… | 通过 |
| zaimanhua | zaimanhua.js | 14981 B | 96b89df7bcdaa2f3… | 96b89df7bcdaa2f3… | 通过 |

## 3. 在线地址可达性（官方 CDN，2026-11-02 实测）

- jsDelivr（cdn.jsdelivr.net/gh/venera-app/venera-configs@main/）：8 个脚本 + index.json 全部 HTTP 200，Content-Type application/javascript，字节数与本地镜像一致。
- raw.githubusercontent.com：存在间歇性连接重置/超时（中国大陆网络常见），建议最终使用 jsDelivr 地址。

## 4. 结论

全部检查：通过。本目录内容可整体上传至 GitHub 公开仓库。
