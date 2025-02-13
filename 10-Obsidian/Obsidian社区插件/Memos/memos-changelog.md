---
uid: 20230913172534
title: Memos 2.X 更新记录
tags: [memos]
description: Obsidian 插件 Memos 2.X 更新记录
author: Bon
type: other
draft: false
editable: false
modified: 20231017111216
---

# Memos 2.X 更新记录

需要请加入内侧体验

[社区众筹插件 (pkmer.cn)](https://pkmer.cn/products/productDetails/)

## memos-v2.0.13 2023.10.08

### 新功能

- 支持在 Theme 设置中实时切换 Heatmap 颜色，已经预留了六种颜色方案

### 修复

- 在 Memos 编辑器中无法输入标签、日期等；
- Memos 在后台时也会响应左侧栏或者右侧栏开闭事件，导致其会重载；
- 会出现浮动左侧栏左侧间距不统一的问题；

### 弃置

- 暂时下线拖动 Memo 功能，现在在 Memo 上划动可以正常选中文本

---

### New Features

- Supports real-time switching of Heatmap colors in Theme settings, with six color schemes already reserved.

### Fixes

- Issues with entering tags, dates, etc. when input in editor;
- When memos is not active, it still responds to the opening and closing events of the left or right sidebar, causing it to reload;
- There are inconsistencies in the left margin of the floating left sidebar.

### Deprecated

- Temporarily removed the drag Memo feature. Now, you can normally select text by swiping on the Memo.

## memos-v2.0.12 2023.10.07

### 新功能

- #亮点 【多文件来源 for MEMOS】具体操作逻辑是设置一个文件夹，在这个文件夹下的所有 Markdown 文件都会被视作 Memos，其它的编辑、归档、删除以及双向编辑都一样；
   - 注意：目前不支持子文件夹
   - 基于上边的操作中，如果发现存在一个 Memos 没有唯一 ID 会在这个 Memos 的右上角显示一个修复按钮，而这个 Memo 因为没有唯一 ID 所以不可编辑；
       - 但是一般情况下会默认直接增加新的 ID；
- #亮点【多文件来源 for MEMOS】检索内容且复制全部 Memo 的时候，Memo 没有正确被处理；
- 编辑器按 Alt+1、2、3 切换保存位置；
- 编辑器按 Ctrl 或 CMD + L 可以快速切换当前的 MEMO 状态；
- 点击左侧栏的随机回顾按钮可以直接更新随机回顾的内容；
- #亮点 修改设置可以实时变化 Memos 的内容，目前支持用户名、保存位置（也就是解析哪个标题下、Memos 文件等）
- 重构了 Memos 的菜单，提供了一个新的选项：复制 Memos 内容以及提供了查看当前的 Memos 字数的功能；
- 只要 Memos 范围内在按 i 会聚焦到编辑器，按 o 会聚焦到搜索框、按 Esc 会退出编辑状态；

### 修复

- #亮点 Memos 首次打开的启动过慢问题，从原来的 320ms 降到 26ms；
- 检索式的标题没办法编辑；
- 筛选没有 Tag 的 Memo 的快捷路径会忽略换行后的 Tag 的 Memo；
- 给部分按钮加上 Tooltip 提示；
- Banner 上的数字过大的时候会很拥挤；

### 变更

- 暂时下线批注 memo 显示内容；
- Memo 多了四个 css 选择器，分别为：data-source-type、data-memo-id、data-memo-type 以及 Pin 与否的选择器；
- 下线了全局切换 Memo 输入状态的命令；
- 移动端不能正常启动的问题；

---

### New Features

- [Multiple File Sources for MEMOS]: The specific operation involves setting up a folder, and all Markdown files under this folder are treated as Memos. Other operations like editing, archiving, deleting, and bidirectional editing remain the same;
   - Note: Subfolders are currently not supported.
   - Based on the above operation, if a Memo is detected without a unique ID, a fix button will be displayed in its top right corner. This Memo is not editable due to the absence of a unique ID;
       - However, in most cases, a new ID will be automatically added by default.
- [Multiple File Sources for MEMOS]: When searching for content and copying all Memos, the Memo isn't processed correctly;
- In the editor, press Alt+1, 2, 3 to switch save locations;
- In the editor, press Ctrl or CMD + L to quickly toggle the current MEMO's status;
- Clicking the random review button in the left sidebar will instantly update the content of the random review;
- Changing settings will reflect real-time changes in Memos' content. Currently supports username, save location (i.e., determining under which title, Memos files, etc.)
- The Memos menu has been refactored, adding a new option: copying the content of Memos and providing a function to view the current word count of Memos;
- Within the Memos scope, pressing 'i' will focus on the editor, pressing 'o' will focus on the search box, and pressing 'Esc' will exit the editing mode;

### Fixes

- Addressed the slow startup issue when Memos are opened for the first time, reduced from 320 ms to 26 ms;
- Query title cannot be edited before;
- NO_TAG will not match memo that using tag in new line;
- Added Tooltip to parts of buttons;
- Numbers on the Banner become congested when they're too large;

### Changes

- Temporarily suspended the feature that annotated memos;
- Memo now includes four additional CSS selectors, specifically: data-source-type, data-memo-id, data-memo-type, and a selector for whether it's Pinned or not;
- The global command to toggle Memo input status has been deactivated.
- Mobile issues；

## memos-v2.0.11 2023.09.28

- #亮点 修复移动端异常，支持 iOS 和 Android

## memos-v2.0.10 2023.09.25

简评：逐步引入多来源来获取 Memo 的功能，重构了样式系统，现在可以用 CSS 变量来控制 Memos 的外观；

### Features

### 功能相关

- #亮点 右键 Ribbon Icon 可以直接控制 Memos 打开的位置，不需要先打开再拖动了；
    - 按住 Ctrl、Shift 以及 Alt 分别是右侧栏、左侧栏、浮窗显示 Memos；
- #亮点 支持设置存入位置为 Canvas，你可以在编辑器中实时调整保存的位置；
    - 当你设置任意的 Canvas 名称为 xxxxx.memos.canvas 的时候，会自动从其中获取 Memos，不过由于不想侵入式修改此前已经存在的卡片，所以只有你修改 canvas 中的卡片或者在 Memos 中输入卡片且设定为插入到 canvas 的情况下，才会对 canvas 中进行 memo 的保存；
    - 注意，默认会保存到 basic.memos.canvas 文件，如果你想要修改这个名字，或者修改路径，请去设置中进行修改；
    - 从插入 canvas 开始，你的所有对通过 memos 插入的 canvas 节点的修改，或者新建成功后的节点的修改，都会如实反应到 memos 列表中，当然反向也会有一样的效果；
    - 未来会扩展到文件夹、单文件以及标签索引等多来源；
- #亮点 新的图片预览器，你可以滚动滚轮（按住 Ctrl）来快速缩放内容，当当前的 Memo 有多个图片的时候，你可以点击上一张以及下一张来切换图片；
- #亮点 每日 Memo 进度条，你可以设定一个每天希望写多少个 Memo 的进度条，而且动态地设置目标，==未来会基于该功能引入统计功能==；
- 当分享 Memo 的时候，会渲染 Markdown 内容，而不是仅展示纯文本；
- 按住 Alt 键会允许你选择复制 Memo 内容；
- 当 Memo 的数目超过 20000 的情况下，会动态调节字体的大小，防止其重叠；
- 提供了一个设置按钮来修复此前的 Flomo 的导入错误；
- 绝大部分的颜色、圆角变量已经提取出来作为 CSS 变量，所以你可以直接修改 CSS 变量来调整 Memos 外观了；
- 随机回顾支持了刷新按钮；

### Fixed

- #亮点 Flomo 的内容应该可以正常导入了；
- #亮点 手机端无法正常使用 Memos；
- a 标签有可能会超出 Memo 的宽度范围的问题；
- 恰好为 40~50 个 memos 的情况下，索引会出错；

## memos-v2.0.10

1、如果 Daily 插件（日记插件）未设置任何文件存储目录的时候，应当以根目录为基础，而不是直接报错退出；

2、当日记文件在不同层级的情况下，应当能适配对应的情况；例如 2023-01-01 在根目录，而 2023-01-02 在子目录的情况下，会不能编辑（之前）

3、当日记文件中不存在 # Journal 标题的情况下也应该能正常解析（如果没有设置指定标题的话）

## memos-v2.0.9

==简评：2.0.9 是一个彻底重构的版本，其性能远远超越了 1.9.7 也远远超越了 2.0.7 （再也不用忍受难以忍受的卡顿了）==

### 性能相关

- 优化初次打开速度，当你打开 Obsidian 的时候，Memos 就会在后台加载，当你需要打开 Memos 的时候不再需要等待；
- #亮点 完美的懒加载，保证你的 Memos 在即使五 5 万以上的 Memos 也不会有过多卡顿；

### UI 相关

- #亮点 侧边栏的快速入口，包括随机回顾、归档以及回收站三个主要入口；
- #亮点 顶部的页面形式切换按钮，可以切换列表或者瀑布流信息加载；
    - 页面缩放的时候会自动切回列表状态；
    - 当鼠标悬浮在时间戳上时可以看到完整的时间戳；
- 顶部的 Day 数字悬浮时可以看到你最早使用 Memos 的时间；
- 顶部新增每日 Daily 的快速入口；
- 更方便的 Pin 或者 Unpin 按钮；
- 归档、回收站均增加了返回 Memos 主页按钮；

### 功能相关

- #亮点 完美支持 Obsidian 的原生渲染器，所以现在只要是 Obsidian 的笔记的 Preview Mode 支持的内容，理论上都可以得到支持；
- #亮点 在页面中任意位置按 i 可以直接跳转到输入框；
- #亮点 在编辑框中按 Ctrl+Enter/Cmd+Enter 可以快速保存内容，而无需再额外设置一个快捷键了；
- 在 Memo 上右键可以查看到编辑菜单；
- 待办、Task Memo 都可以直接切换状态了，只需要点击一下；

### Fixed

- #亮点 小狼毫输入法可以正常输入了
- 删除笔记、编辑笔记以及新建笔记都会按部就班地对 Memos 中的 Memo 做出改动；
- 导出图片以及每日日记都支持了 web 的图片；
- 粘贴图片可能会插入两次图片；
- 编辑内容有可能保存不成功；
- Memo 总数有些时候可能统计不准确；
- 删除 Memo、归档 Memo 的时候可能出现没有归档成功和删除成功的情况；