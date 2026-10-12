# 学术主页：个人资料填写示例与编辑指南

> 此文件和 index.html 位于 `academic-homepage-draft` 草稿分支。
> 当前所有姓名、经历、论文和奖项都是格式占位，不代表真实资料。
> 仓库的 GitHub Pages 从 `main` 分支发布；不要合并草稿、不要修改 Pages 来源，直到你决定正式发布。
> 草稿分支不是隐私功能：公开仓库里的文件仍然公开可见。请勿提交密码、令牌或私人资料。

## 直接在 GitHub 中完成填写

1. 打开仓库，确认左上角分支是 **academic-homepage-draft**，不是 main。
2. 打开本文件，点击铅笔图标（Edit this file），按下方示例整理你的资料。
3. 点击 **Commit changes**，选择直接提交到 **academic-homepage-draft**。
4. 打开同分支的 `index.html`，点击铅笔图标，将实际资料填入对应位置。HTML 内有“填写 1”到“填写 5”的中文注释。
5. 编辑完继续提交到草稿分支；不要点击 Merge，也不要把草稿设为 Pages 发布分支。

**注意：修改本 Markdown 文件不会自动更新主页。它是资料填写表；页面内容需要对应修改 index.html。**

## 预览（不发布）

GitHub 文件页只显示 HTML 源码，不会直接渲染网页。可在草稿分支选择 **Code → Download ZIP**，解压后双击 `index.html` 用浏览器打开。页面无需安装任何依赖，支持离线预览。

## 一、基本信息

- 中文姓名：［你的中文姓名］
- 英文姓名：［Your Full Name］
- 当前身份：［例如 Ph.D. Student / Master's Student / Research Assistant］
- 学校或机构：［机构中英文名称］
- 院系：［院系中英文名称］
- 导师：［导师姓名及主页 URL；不适用则删除］
- 城市 / 国家：［愿意公开的信息］
- 学术联系邮箱：［你的公开邮箱］
- Google Scholar：［完整 URL；没有则删除］
- GitHub：［完整 URL］
- 个人简历：［assets/cv.pdf；没有则删除］
- 头像：［assets/avatar.jpg］

### 英文简介格式示例

I am a [position] in the [Department] at [University], advised by [Advisor]. I received my [degree] in [major] from [University] in [year]. My research interests include [topic A], [topic B], and [topic C]. I am particularly interested in [specific problem or goal].

### 中文简介格式示例

我是［学校/机构］［院系］的［身份］，导师为［姓名］。我于［年份］在［学校］获得［专业］［学位］。我的研究主要聚焦［方向］，尤其关注［具体问题］。

## 二、研究方向

- ［研究方向一］
- ［研究方向二］
- ［研究方向三］

## 三、教育经历（每段重复此组）

- 学校：
- 学位 / 专业：
- 起止时间：YYYY.MM – YYYY.MM / Present
- 导师（可选）：

## 四、论文（每篇重复此组，没有论文可删除整个栏目）

- 标题：
- 作者（按照论文署名顺序）：
- 自己的署名：
- 会议 / 期刊 / 预印本名称：
- 年份：
- 状态（已发表 / 已接收 / 预印本）：
- 论文 URL：
- 代码 URL（可选）：
- 项目 URL（可选）：
- 论文配图（可选，例如 assets/paper-1.png）：
- 共同一作等备注（必须属实）：

## 五、最新动态

- YYYY.MM：［一条真实学术动态］
- YYYY.MM：［一条真实学术动态］

## 六、科研 / 实习经历

- 机构和团队：
- 职位：
- 起止时间：
- 一句话介绍项目及个人贡献：

## 七、荣誉与学术服务

- 奖项：［名称］，［颁奖机构］，［年份］
- 学术服务：［角色］，［会议或期刊］，［年份］

---

# 修改 index.html 的具体示例

## 替换姓名、职位与研究方向

搜索 `Your Name` 并替换为你的英文名；另行替换中文姓名、学校和职位。还需修改 `<title>`、description 和页脚。

所有方括号 `[ ... ]`、`YYYY`、`SAMPLE CONTENT` 和 `待添加` 都是占位标记。请替换或删除，不要保留虚构信息。

## 添加头像和简历

在草稿分支的 `assets` 文件夹使用 **Add file → Upload files** 上传头像和 PDF，并提交到草稿分支。

将整个头像占位块 `<div class="portrait" ...>...</div>` 替换为：

```html
<img class="portrait" src="assets/avatar.jpg" alt="你的姓名">
```

在侧栏加入简历链接：

```html
<li><a href="assets/cv.pdf">Curriculum Vitae</a></li>
```

文件名大小写必须与上传文件一致。

## 添加邮箱和社交链接

当前页面的邮箱、Scholar、GitHub 和资源按钮是普通文字占位。请替换为真实链接：

```html
<li><a href="mailto:your.name@example.com">Email</a></li>
<li><a href="https://scholar.google.com/citations?user=YOUR_ID">Google Scholar</a></li>
<li><a href="https://github.com/YOUR_USERNAME">GitHub</a></li>
```

以上 URL 本身也是格式示例，必须替换为你的真实地址。

## 添加论文链接和配图

复制整个 `<article class="pub">...</article>` 添加论文。作者顺序应与原文一致；用 `<strong>` 标出自己的姓名。

把资源文字替换为链接：

```html
<a class="resource" href="https://arxiv.org/abs/YOUR_PAPER_ID">Paper</a>
<a class="resource" href="https://github.com/OWNER/REPO">Code</a>
```

将论文图占位块替换为：

```html
<img class="figure" src="assets/paper-1.png" alt="论文方法示意图">
```

如果不需要配图，删除 figure 块，并为对应 article 添加 `style="grid-template-columns:1fr"`。

## 删除不适用栏目

删除对应的整个 `<section>...</section>`；如果该栏目在顶部导航出现，也删除指向它的链接。例如删除 Publications 后，应同时删除 `href="#publications"` 的导航链接。

## 将来准备发布时再做

- 检查全部事实、姓名、时间和外部链接。
- 删除顶部 `.demo` 模板提示、简介 `.hint` 填写提示、SAMPLE CONTENT、Placeholder examples 和页脚 Draft。
- 更新 `<title>` 与 description。
- 准备公开并允许搜索后，再删除 `<meta name="robots" content="noindex,nofollow">`。该标签不是保密功能。
- 确认所有照片和论文图片有使用权限。
- 明确决定发布后，才将草稿合并进 main；目前不要合并。

页面为原创静态 HTML/CSS，内容组织参考用户提供的学术主页示例，不复制参考作者的个人资料或图片。无 JavaScript、无外部依赖、无统计跟踪。
