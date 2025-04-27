# SVG Fill Rule Converter: Even-Odd to Non-Zero

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

这是一个简单的 HTML 页面，用于演示或提供将 SVG 路径元素的 `fill-rule` 属性从 `evenodd` 转换为 `nonzero` 的功能。

## 为什么需要这个转换？

SVG 的 `fill-rule` 属性决定了如何判断一个点是否在形状内部。

* **`evenodd` (奇偶填充):** 通过从该点向任意方向绘制一条射线，并计算形状轮廓线与该射线的交点数。奇数表示在内部，偶数表示在外部。
* **`nonzero` (非零填充):** 通过绘制射线并跟踪轮廓线的穿过方向（顺时针 +1，逆时针 -1），如果卷绕数之和不为零，则在内部。

在处理由多个重叠路径组成的复杂 SVG 时，`nonzero` 往往能提供更符合预期的填充效果。

## 如何使用

1.  **打开 `index.html` 文件** (假设你的 HTML 文件名为 `index.html`)：在你的浏览器中直接打开这个 HTML 文件。
2.  **上传 SVG 图标：** 在页面提供的上传控件上传 SVG 图标。
3.  **点击转换按钮：** 点击页面上的按钮开始转换。
4.  **查看转换结果：** 转换后的 SVG 支持批量保存。

## 功能

这个 HTML 页面提供了一个简单的界面，用于：

* 接收用户输入的 SVG 代码。
* 自动检测并替换 SVG 路径元素中的 `fill-rule="evenodd"` 为 `fill-rule="nonzero"`。
* 实时显示转换后的 SVG 代码。

## 局限性

* 这是一个简单的客户端工具，所有的转换都在浏览器中完成。
* 目前只关注 `fill-rule` 属性的转换，不会修改 SVG 的其他部分。
* 可能无法处理非常复杂的或格式不规范的 SVG 代码。

## 贡献

欢迎通过提交 issue 的方式报告问题或提出建议。

## 许可

本项目基于 [MIT 许可证](https://opensource.org/licenses/MIT) 开源。

-----

这个 README 文件更侧重于介绍一个直接在浏览器中运行的 HTML 工具。记得将 `index.html` 替换为你实际的 HTML 文件名。如果你的 HTML 页面有更具体的功能或交互方式，可以在 "功能" 部分进行更详细的描述。
