# 设计方向配方

```toml
format = "recipkg/1"

[package]
name = "design-directions"
version = "0.1.2"
kind = "software"
description = "面向不同产品任务选择与验证视觉方向的设计合同。"
entry = "BUILD_PROMPT.md"

[dependencies.foundation]
git = "https://github.com/recipkg/design-foundations.git"
rev = "8c5bf1f1e40719789cf51bc0dfd8f5aeecae0538"
```

本包提供设计方向和选择方法，依赖 `foundation` 提供交互、响应式和无障碍质量底线；它不是某个厂商的设计系统副本。
