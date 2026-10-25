# 𝕏 Algorithm 中文摘要

本仓库保存对 𝕏 官方推荐算法开源仓库的中文总结，供浏览器扩展读取。

## 数据文件

- [`data/summary.json`](data/summary.json)：当前算法规则摘要、公开默认权重、来源 Commit 与源文件 Blob SHA。
- [`data/history.json`](data/history.json)：按上游变更增量维护的中文更新历史。

## 上游来源

- [xai-org/x-algorithm](https://github.com/xai-org/x-algorithm)
- [README.md](https://github.com/xai-org/x-algorithm/blob/main/README.md)
- [home-mixer/params/param.rs](https://github.com/xai-org/x-algorithm/blob/main/home-mixer/params/param.rs)
- [xai-value-model/scoring.rs](https://github.com/xai-org/x-algorithm/blob/main/xai-value-model/scoring.rs)

## 更新原则

ChatGPT 定时任务每 12 小时检查一次上游。只有跟踪的源文件发生变化时，才更新中文摘要和历史记录；权重变化会记录旧值、新值与差值。写入通过单个 Git 提交发布，避免摘要和历史只更新一半。

所有权重均是公开代码中的默认值，不等于某个用户的实际线上配置。权重乘以模型预测概率或连续预测值，不乘原始互动次数。公开仓库也明确说明，部分 Grox 提示文件和部分 botmaker 规则未公开。

摘要是对公开材料的解释，不应被当成未公开的生产配置或对实际曝光量的精确预测。
