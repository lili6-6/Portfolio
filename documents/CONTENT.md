# CONTENT.md — 内容与代码规范

> 本规范定义 `index.html` 中静态资源引用、JavaScript 数据维护及描述风格。
> 配合 `AGENTS.md` 使用。

---

## 一、路径格式

`index.html` 中所有静态资源使用**相对路径**，格式固定为：

```html
<!-- 图片 -->
<img src="img/project1_1.jpg" alt="描述" />

<!-- 视频 -->
<video src="video/glowborn.mp4" poster="img/project2_1.jpg"></video>
```

**规则：**
- 路径必须以 `img/` 或 `video/` 开头，不加 `./` 前缀
- 图片 `alt` 属性必须填写中文描述
- 视频 `poster` 属性引用对应的封面图

---

## 二、JS 数据维护

项目中所有数据定义在 `index.html` 内 `<script>` 标签的常量中：

| 常量名 | 用途 |
|---|---|
| `skills` | 技术能力模块（6项） |
| `projects` | 项目作品数据（6项） |
| `awards` | 获奖经历列表 |
| `certificates` | 证书图片列表 |
| `filters` | 筛选分类 |

修改内容时直接编辑对应数组即可，CSS 样式集中在前部的 `<style>` 中。

---

## 三、内容描述风格

**所有项目描述、时间线描述、标签描述必须偏技术向**，面向技术岗面试官阅读：

- 使用技术术语描述系统实现，而非游戏体验感受
- 强调架构设计、模块划分、技术选型、实现手段
- 时间线描述格式：`核心技术点1、核心技术点2、...`
- 标签（tags）优先使用技术关键词（如 `ScriptableObject`、`行为树`、`RenderTexture`），而非泛化形容词
- 如有不确定如何用技术语言表达的内容，向作者（刘嘉琳）确认补充
