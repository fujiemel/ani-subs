# ani-subs

Animeko 的数据源订阅。公开仓库，方便手机/其他设备直接订阅。

## 是什么

Animeko 的「数据源」是一个 JSON 订阅，客户端按里面的 CSS 选择器去第三方站抓番剧资源。
这个仓库用来存放筛选过、能用的那部分源，并生成一个可以直接订阅的地址。

## 订阅地址

首选（jsDelivr CDN 加速，国内可直连）：

```
https://cdn.jsdelivr.net/gh/fujiemel/ani-subs@main/ani-subs.json
```

在 Animeko 里：设置 → 数据源管理 → 添加订阅 → 粘贴上面的地址。

> jsDelivr 有缓存：仓库更新后，巡查任务会主动刷缓存，一般几分钟内生效；等不及可换下面的实时地址。
> 备用 1（ghfast 实时代理，无缓存延迟）：`https://ghfast.top/https://raw.githubusercontent.com/fujiemel/ani-subs/main/ani-subs.json`
> 备用 2（GitHub 原始地址，国内可能打不开）：`https://raw.githubusercontent.com/fujiemel/ani-subs/main/ani-subs.json`

## 文件

```
ani-subs.json        订阅本体（schemaVersion 2，Animeko 4.9+）
sources/             单个源的原始配置，便于单独维护
notes/health.md      体检记录：哪些源活着、卡在哪一层
```

## 评级口径

```
L0  搜索页都打不开
L1  页面能开但选择器匹配 0 条（站改版了）
L2  能搜到番，详情页解析不出剧集
L3  能出剧集列表
L4  播放页能拿到 m3u8，且直链真返回 #EXTM3U
```

只发布 L3 及以上；L4 才有资格进 tier 0。

## 免责

所有源都指向第三方站点，本仓库只保存「怎么抓」的配置，不托管、不分发任何视频内容。
第三方站点的可用性、合法性由各站点自负，配置失效属于常态。
