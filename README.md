# Nginx + Coraza WAF 自动构建

自动编译静态内置 [Coraza WAF](https://github.com/corazawaf/coraza-nginx)（libcoraza + coraza-nginx）的 Nginx，定时检查上游更新并发布。

## 最新版本

- **版本**：`v1.31.4-coraza-ce4238f`
- **构建时间**：2026-08-24 23:36 UTC

## 下载

| 架构 | 产物 |
| --- | --- |
| linux/amd64 (glibc, Ubuntu 24.04) | [nginx_custom.tar.gz](https://github.com/ylx2016/Hestia_nginx_coraza/releases/latest/download/nginx_custom.tar.gz) |

解压后包含 `nginx` 二进制与 `lib/libcoraza.so` 引擎库。

[查看全部 Release](https://github.com/ylx2016/Hestia_nginx_coraza/releases)

## 说明

- 定时任务每周日 03:17 UTC 运行，仅当 Nginx 有新版本或 coraza-nginx 有新提交时才编译；手动触发则强制重编。
- 始终使用 nginx.org 最新版本与最新稳定版 Go 编译。
- 固定在 Ubuntu 24.04 上编译，确保 glibc 版本与 HestiaCP 目标环境兼容。
- 每次构建都会更新本 README，以此产生提交、保持仓库活跃，避免 GitHub 因「60 天无活动」自动停用定时任务。
- 仅保留最新 3 个 Release。

<!-- 本文件由 GitHub Actions 自动生成，请勿手动编辑 -->
