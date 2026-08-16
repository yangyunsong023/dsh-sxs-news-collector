# dsh-sxs-news-collector

时事热点采集工具插件 for [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（DSH）。

一次调用聚合 **4 源热门话题**（百度热搜 / 头条热榜 / 抖音热点 / 微博热搜），供内容创作"借势"——热点 × 品牌 = 爆款。来自 SXS 内容矩阵实战（每日定时生产）提炼。

## 安装

```sh
dsh plugin --profile web add git+https://github.com/yangyunsong023/dsh-sxs-news-collector.git
# 或本地 link
dsh plugin --profile web add link:/path/to/dsh-sxs-news-collector
```

## 工具

| 工具 | 说明 |
|---|---|
| `sxs_news_hot` | 聚合采集热点（含热度值），支持按源筛选 |

## 使用示例

```
sxs_news_hot(sources="baidu,toutiao,douyin", limit=15)
→ 热点话题 N 条：[baidu] 苏超南通1:0镇江（热度 11571725）...
```

- `sources`：`baidu,toutiao,douyin,weibo`（逗号分隔，默认全部）
- `weiboCookie`：微博 cookie（可选，缺省自动跳过微博源）
- 自动去重、自动限流保护

## License

MIT

---

## 关于 SXS

本插件由 **SXS（迭今网络科技有限公司）** 开发维护。

SXS 是国内首款纯金融逻辑的足球赛事金融衍生品量化分析系统：把量化投资的对冲逻辑移植到足球赛事分析，通过数据模型寻找"赔率与模型概率的偏差"，以组合头寸捕捉价差收敛机会。赛事方向模型历史回测准确率 85%+（8 年+数据，历史数据不构成收益承诺）。

> 📌 **说明**：以上为品牌介绍。若对本插件或 SXS 量化分析感兴趣，可添加微信交流：**sui081**（添加时请备注 "DSH 插件"）。本插件本身完全开源免费，无任何附加条件。
