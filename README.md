# Attention Residuals 交互式讲解

一个单文件、离线可执行的交互式动画网站，用可视化的方式一步步讲解 Kimi K3 的 **Attention Residuals（注意力残差）** 机制。

## 特点

- **单文件离线运行**：`index.html` 包含所有 HTML / CSS / JS，双击即可打开，无需网络、无需构建、无需安装依赖。
- **响应式多端兼容**：适配桌面端与移动端，自动调整画布布局。
- **8 步交互式讲解**：从标准 Transformer 残差的问题出发，逐步引入 Attention Residuals、Query 学习、Block Attention Residuals 与核心收益。
- **可交互 playground**：自由调整层数与块大小，观察 Block Attention Residuals 的检索范围。

## 使用方法

1. 直接双击 `index.html` 用浏览器打开。
2. 点击「开始交互讲解」，跟随步骤学习。
3. 使用 ← / → 键或按钮切换步骤，鼠标悬停查看细节。

## 文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 完整交互式网站（唯一运行文件） |
| `design.md` | 设计文档 |
| `README.md` | 本说明 |

## 核心知识点

- 标准残差连接在深层网络中会导致早期信息稀释。
- Attention Residuals 将注意力机制从「序列维度」转到「深度维度」，让每一层都能直接访问前面所有层。
- 每层的 Query 是训练中学到的参数向量，决定该层「想检索什么」。
- Block Attention Residuals 通过分块降低通信开销，将复杂度从 O(L²) 降到 O(N·d)。

## 技术栈

- 原生 HTML5 / CSS3 / Canvas 2D
- 零外部依赖，零 CDN
- 原生 ES6 JavaScript
