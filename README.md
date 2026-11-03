# BW的Python家园 · BW's Python Home

一个可以直接在浏览器里用的 Python 刷题与复习工具：**599 道题、错题间隔复习、AI 助教、代码练习**。
打开即用，不需要注册，不需要安装。

> An all-in-one Python quiz & review web app: 599 questions, spaced-repetition review, AI tutor, and an in-browser Python playground. No sign-up, no install.

**在线使用 / Live demo：** <https://bw448.github.io/bw_python/>

---

## 中文

### 功能

| 功能 | 说明 |
|---|---|
| 题库 | 10 套卷共 599 题：单选 300、多选 150、填空 50、代码阅读 50、设计 49 |
| 按套练习 | 按原卷顺序刷，可只刷某一种题型 |
| 随机练习 | 按数量、题型随机抽题 |
| 搜索 / 收藏 | 搜题干、选项、解析；题目右上角星标收藏 |
| 错题复习 | 答错后按 1 / 3 / 7 / 14 / 30 天间隔复习，连对 5 次毕业 |
| 答题历史 | 每次作答都有记录，按天分组，可点开重做 |
| 每日目标 | 每天 10 / 20 / 30 / 50 题，记录连续打卡 |
| 十天冲刺 | 内置 10 天练习安排，每天一键开始 |
| 模拟考试 | 单选 / 多选 / 填空，限时 60 / 90 / 120 分钟 |
| AI 助教 | 讲解题目、批改代码、解释报错、解释选中文字；支持多轮追问和历史对话 |
| 代码练习 | 多文件、行号、语法高亮、代码补全，浏览器内运行 Python，支持 numpy / pandas / matplotlib |
| PWA | 添加到手机主屏，缓存后断网也能打开 |

### 手机上使用

1. 手机浏览器打开 <https://bw448.github.io/bw_python/>
2. **iPhone**：Safari → 分享 → 添加到主屏幕
3. **Android**：Chrome → 菜单 → 安装应用 / 添加到主屏幕

安装后从主屏图标打开，页面和图标会被缓存，**断网也能刷题**（第一次安装需要联网）。

### AI 怎么用

AI 功能需要你自己的 DeepSeek API Key：

1. 首页右上角 **AI** → **配置 AI**
2. 填入 `sk-...`，点「测试连接」→「保存」
3. Key 只保存在你自己的浏览器里，只会发送给 `api.deepseek.com`

### 数据与隐私

- 做题记录、错题、收藏、历史、API Key 全部存在**浏览器 localStorage**
- 不上传服务器，不需要注册，不收集个人信息
- 换浏览器、清缓存会丢失数据；建议固定用同一个浏览器

### 本地使用

- 直接双击 `刷题.html` 即可（PWA 需要 https，本地不生效）
- 想重新生成页面：改题库后运行 `python build.py`

### 技术栈

- 单文件 HTML + 原生 JavaScript，无框架
- CodeMirror 5（编辑器）、Pyodide（浏览器内 Python）
- DeepSeek API（Anthropic 兼容之外的 OpenAI 风格接口）
- GitHub Pages 托管 + Service Worker 离线缓存

### 目录

```
index.html            主页面（由 _template.html + 题库构建）
manifest.webmanifest  PWA 配置
sw.js                 Service Worker 离线缓存
icons/                网站图标
```

> 题库内容来自课程复习资料，仅用于学习交流。

---

## English

### What it does

| Feature | Description |
|---|---|
| Question bank | 599 questions across 10 papers: single choice, multiple choice, fill-in, code reading, design |
| Practice modes | By paper, random by type/count, favorites, due review |
| Search & favorites | Full-text search over stems, options and explanations; star any question |
| Spaced repetition | Wrong answers return after 1 day, then 1 / 3 / 7 / 14 / 30 days; graduate after 5 correct |
| Answer history | Every attempt is logged, grouped by day, click to retry |
| Daily goal | 10 / 20 / 30 / 50 questions per day, with streak tracking |
| 10-day plan | A built-in study schedule with one-click start |
| Mock exam | Single/multiple/fill, timed 60 / 90 / 120 minutes |
| AI tutor | Explain questions, grade code, explain errors, explain selected text; chat history |
| Code playground | Multi-file editor with syntax highlighting, completion, and in-browser Python (numpy / pandas / matplotlib) |
| PWA | Installable, works offline after the first load |

### Use it

Open <https://bw448.github.io/bw_python/> in a browser. On mobile, use “Add to Home Screen” to install it as an app.

### AI setup

Bring your own DeepSeek API key: click **AI → Configure**, paste `sk-...`, test and save. The key stays in your browser and is only sent to `api.deepseek.com`.

### Privacy

All progress, favorites, history and the API key are stored in your browser's `localStorage`. Nothing is uploaded, and there is no sign-up.

### Tech

Vanilla HTML/JS in a single page, CodeMirror 5, Pyodide, DeepSeek API, GitHub Pages + Service Worker.

---

## License / 许可

Code: MIT. Question content belongs to the original course materials and is provided for study purposes only.
