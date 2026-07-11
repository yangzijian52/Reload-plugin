# Reload Paper 26.2 升级说明

## 概要

本文档记录 `Reload` 对 `Paper 26.2` 的兼容升级情况。

- 项目版本：`1.0.2`
- 目标 Paper API：`26.2.build.56-alpha`
- 所需 Java 版本：`25+`
- 升级日期：`2026-07-11`

## 本次调整

- 项目版本从 `1.0.1` 升级为 `1.0.2`
- Paper API 从 `26.1.1.build.20-alpha` 升级为 `26.2.build.56-alpha`
- 保持 Java `25` 编译目标与现有插件功能不变

## 说明

- 插件在升级前即可兼容 Paper 26.2，本次仅更新编译依赖和发布版本信息
- 按发布要求不重复进行服内运行测试
- 发布前执行 Maven 构建，确认源码可针对 Paper 26.2 API 正常编译打包

## 验证记录

1. 使用 `Java 25` 运行 `mvn clean package`
2. 确认生成 `Reload-1.0.2.jar`
