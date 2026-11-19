# wb-imghost 临时图床

给 AI 生图服务提供临时公网图片直链，图片由 GitHub Actions 每天自动清理。

## 直链格式

https://cdn.jsdelivr.net/gh/feizhaiV/wb-imghost@main/imgs/文件名

## 使用

1. 把图片放入 imgs 目录并 push
2. 用上面的格式拼直链，喂给生图服务
3. 无需手动删除，定时任务自动清理

## 清理策略

每天北京时间 11:00 执行，删除 imgs 下超过 3 天的图片。
保留天数在 .github/workflows/cleanup.yml 里改 mtime 参数。

## 注意

本仓库为 Public（jsDelivr 只加速公开仓库），请勿上传敏感图片。
