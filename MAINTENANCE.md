# 首页维护说明

网站地址：https://yifann-lu.github.io/

首页采用独立的 `index.html`，样式已经包含在里面。项目和文章由 `links.js` 管理。原来的 `README.md` 继续作为仓库说明；修改 README 不会改变新的首页。

## 第一次上传这版首页

1. 解压 `yifan-homepage.zip`。可以先双击 `index.html`，在自己的浏览器里查看效果。
2. 打开 https://github.com/yifann-lu/yifann-lu.github.io/upload/main 。
3. 将 `index.html`、`links.js` 和 `MAINTENANCE.md` 三个文件一起拖入上传区。上传的是解压后的文件，不是 ZIP，也不要套一层文件夹；它们应与原来的 README.md 放在同一级。
4. 点击 **Commit changes**，提交到 `main`。
5. 等现有的 GitHub Pages 自动发布完成，打开网站查看。

## 添加项目或文章

1. 在仓库中打开 `links.js`，点击铅笔图标编辑。
2. 在 `projects` 或 `articles` 的方括号中新增一条记录。
3. 点击 **Commit changes**，提交到 `main`。
4. 等待 GitHub Pages 发布完成，刷新网站查看。

下面是填写后的完整示例。请将示例标题、介绍、地址和日期替换为真实内容后再使用：

```javascript
window.HOME_LINKS = {
  projects: [
    {
      title: "我的 Agent 项目",
      description: "一句话说明项目解决了什么问题。",
      url: "https://github.com/你的用户名/你的项目仓库",
      tags: ["Agent", "Python"]
    }
  ],
  articles: [
    {
      title: "我的第一篇技术笔记",
      description: "文章的简短介绍。",
      url: "https://你的文章地址",
      category: "技术笔记",
      date: "2026-09-11"
    }
  ]
};
```

- **新增多条**：复制一个 `{ ... }`，在相邻两条之间加英文逗号。
- **调整顺序**：直接移动记录，网页按文件顺序显示。
- **删除记录**：删除对应的 `{ ... }`，检查相邻的逗号。
- **分类**：可写“技术笔记”“阅读思考”“生活记录”，或自己起名。
- **日期**：建议使用 `YYYY-MM-DD`，也可以省略。
- **链接**：可以指向 GitHub 仓库、已经发布的文章、项目演示或站内页面。以 `https://` 开头的外链会在新标签页打开。
- **尚未准备好链接**：写 `url: ""` 或省略 `url`，页面会显示为“整理中”。
- **没有任何记录**：页面会显示简洁的待发布提示。添加第一条后，提示自动隐藏。

这个首页只展示文章链接，不负责创建链接所指向的文章内容。以后可以在本仓库添加文章页，也可以链接到其他平台的文章。

## 修改名字、介绍和导航

打开 `index.html`，用浏览器搜索找到：

- `修改首页自我介绍的位置`：修改首页问候语和简介。
- `修改导航文字和目标链接的位置`：修改菜单名称和目标位置。
- `about-copy`：靠近文件后半部分的 `<div class="about-copy">` 中是“关于我”的正文。
- `avatars.githubusercontent.com`：当前使用 GitHub 头像，可以替换为自己的图片地址。

导航里的 `#projects`、`#writing`、`#about` 是当前页面的三个位置。要跳转到其他网页，可以把相应的 `href` 换成完整网址。

## 更新后没有变化

1. 在仓库的 **Actions / 操作** 中查看最新的 Pages 发布任务是否完成。
2. 发布完成后使用 `Ctrl + F5` 刷新网页。
3. 如果添加链接后列表仍为空，先检查 `links.js` 中的引号、逗号、括号是否完整。可对照上面的完整示例。

页面不依赖 npm 或额外的后端服务，继续使用现有的 GitHub Pages 发布设置即可。
