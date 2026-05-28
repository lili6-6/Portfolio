# ASSETS.md — 资产规范

> 本规范定义作品集所有静态资产（图片、视频）的命名、格式与上传规则。
> 配合 `AGENTS.md` 使用。

---

## 一、上传规则

**只上传以下文件/文件夹到 GitHub：**

| 文件/目录 | 说明 |
|---|---|
| `index.html` | 作品集核心页面 |
| `img/` | 所有图片素材 |
| `video/` | 所有展示视频 |
| `README.md` | 仓库说明 |
| `AGENTS.md` | 维护规范 |
| `ASSETS.md` | 资产规范 |
| `WORKFLOW.md` | 工作流规范 |
| `CONTENT.md` | 内容规范 |

**严禁上传：**
- 本地 Unity 项目文件夹（`3d音游/`、`glowBorn/`、`halfWay/` 等）
- `.docx`、`.pptx` 等文档文件
- `简历/` 等个人隐私文件夹
- `index旧.html` 等历史备份文件
- 任何 `.git/` 以外的临时文件

---

## 二、图片命名 (`img/`)

| 类型 | 命名格式 | 示例 |
|---|---|---|
| 项目截图 | `project{N}_{序号}.{jpg\|png}` | `project1_1.jpg`、`project6_1.png` |
| 项目子截图 | `project{N}_app{序号}.{jpg\|png}` | `project1_app1.jpg` |
| 项目特殊图 | `project{N}_{描述}.{jpg\|png}` | `project2_steam.jpg`、`project2_boss.jpg` |
| 获奖证书 | `award{N}.jpg` | `award1.jpg` ~ `award7.jpg` |
| 其他素材 | 全小写英文，下划线分隔 | `ccf_poster.jpg`、`github_qrcode.jpg` |

**规则：**
- 全部使用英文小写 + 下划线，**禁止**中文文件名
- 图片格式统一为 `.jpg` 或 `.png`（项目6 使用 `.png`，其余为 `.jpg`）
- 项目编号 `project1` ~ `project6` 必须与 `index.html` 中的 JavaScript `projects` 数组顺序一致

---

## 三、视频命名 (`video/`)

| 项目 | 视频文件名 |
|---|---|
| 3D音游手机系统 | `rhythm-phone-system.mp4` |
| GlowBorn / 光裔 | `glowborn.mp4` |
| 情绪漂流瓶 | `emotion-drift-bottle.mp4` |
| HalfWay / 中途 | `halfway.mp4` |
| Kinect 皮影动捕 | `kinect-shadow.mp4` |
| 遗忘之匣·回响 | `CasketOfOblivion.mp4` |

**规则：**
- 格式统一为 `.mp4`，H.264 编码
- 命名使用英文小写 + 连字符（`-`），**特殊保留原名**（如 `CasketOfOblivion.mp4` 保持原样）
- 单个视频建议 **控制在 50MB 以内**，总视频大小不超过 200MB

---

## 四、文件质量要求

| 项目 | 要求 |
|---|---|
| 图片格式 | JPG（质量 85%+）或 PNG（截图类） |
| 图片尺寸 | 推荐 1920×1080 或同比例，单张不超过 2MB |
| 视频格式 | MP4 / H.264 |
| 视频尺寸 | 推荐 1080p，码率 2-5 Mbps |
| 视频大小 | 单个不超过 50MB，总数不超过 200MB |
| 代码编码 | UTF-8（无 BOM） |
