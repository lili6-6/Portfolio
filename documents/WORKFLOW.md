# WORKFLOW.md — 工作流规范

> 本规范定义 Git 操作流程、提交信息格式与 `.gitignore` 维护规则。
> 配合 `AGENTS.md` 使用。

---

## 一、Git 命令行方式（推荐）

```powershell
# 1. 进入项目目录
cd "D:\作品集"

# 2. 拉取远程最新（避免冲突）
git pull origin main

# 3. 添加修改的文件
git add img/ video/ index.html README.md

# 4. 提交（使用中文描述）
git commit -m "更新: 简述改了什么"

# 5. 推送
git push origin main
```

---

## 二、首次上传或强制更新

如果拉取失败（网络问题），可采用强制推送：

```powershell
git add img/ video/ index.html README.md
git commit -m "更新作品集文件"
git push origin main --force
```

> ⚠️ 强制推送会覆盖远程提交历史，仅在必要时使用。

---

## 三、网络问题应对

- **无法连接 GitHub**：检查代理/VPN 设置
- **推送超时**：视频文件过大，考虑压缩后再上传
- **SSH 失败**：检查密钥是否添加到 GitHub Settings → SSH Keys

---

## 四、提交信息规范

```
类型: 简短描述

可选详细说明
```

| 类型 | 说明 | 示例 |
|---|---|---|
| `新增` | 添加新项目/新图片/新功能 | `新增: 遗忘之匣项目展示` |
| `更新` | 替换/修改已有内容 | `更新: 替换获奖证书图片` |
| `修复` | 修复 bug 或路径错误 | `修复: 情绪漂流瓶视频路径` |
| `优化` | 改善性能/代码/压缩 | `优化: 压缩视频大小` |

---

## 五、检查清单（每次上传前）

- [ ] `index.html` 中引用的所有图片/视频路径与实际文件名一致
- [ ] 新增的图片/视频已放到 `img/` 或 `video/` 目录
- [ ] 文件命名符合 `ASSETS.md` 规范
- [ ] 没有误传本地项目文件夹或隐私文件
- [ ] 浏览器打开 `index.html` 本地预览通过
- [ ] 提交消息清晰描述了改动内容

---

## 六、.gitignore 维护

当前 `.gitignore` 内容：

```gitignore
*               # 忽略所有文件
!img/           # 保留 img 目录
!img/**
!video/         # 保留 video 目录
!video/**
!index.html     # 保留主页面
!README.md      # 保留说明文件
!.gitignore     # 保留自身
```

如需新增允许上传的文件/目录，在 `.gitignore` 追加 `!` 解除忽略。例如：

```gitignore
!AGENTS.md      # 保留本规范文件
```
