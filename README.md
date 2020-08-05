# Bubble

Typecho 清新风格响应式主题。

化繁为简，如沐清风。

Demo:  [https://tntofu.com/](https://tntofu.com/)

如果觉得本主题还不错的话可以给个 star 哦，这是对开源主题作者们最大的鼓励。

# 特性

+ 清新的界面：大气简洁的页面布局，采用 argon design system，元素间隔恰到好处
+ 人性化的设计：登陆后显示后台管理按钮、醒目的文字、方便操作的按钮摆放，以及页面自适应
+ 流畅的用户体验：支持全站 pjax、ajax 实现评论无刷新，采用 jsDelivr CDN 全球加速主题大部分静态资源加载，减小服务器压力
+ 短代码功能：使用主题特殊 HTML 标签实现更丰富的功能，如高亮代码框以及友链卡片
+ 自定义壁纸：首页固定壁纸、其他页面随机壁纸，彰显个性爱好
+ 代码高亮：自带 prism.js 代码高亮，主题丰富，解析迅速
+ 数学公式：自带 KaTeX 数学公式渲染，相比 MathJax 更为轻量、快速
+ 自定义样式：支持用户添加 css 样式，随意调整主题外观
+ 文件轻量：主题`.zip`格式安装包（去掉`.git`文件夹后）大小不到 250 KB，简洁而不简单

~~我真佩服自己写文案的水平。~~

# 使用
## 安装

在 [Releases](https://github.com/trinitrotofu/Bubble/releases) 下载 zip 源码，解压后移动到 Typecho 主题目录。

## 设置

主题设置页面位置：Typecho 后台->控制台->外观->设置外观。

## 更新

主题有自动检查更新功能，并且能够一键安装更新。

自动更新按钮设置在主题设置页面中。

自动更新将从 jsdelivr 的 CDN 上下载最新版本的主题以替换旧版本主题。

你也可以手动更新，手动更新步骤为：删除旧版本，并安装新版本。

请注意，由于 Typecho 本身设计的原因，主题更新后可能会添加新的设置项，如果不禁用主题并重新启用（通过启用其他主题），新设置项将被留空并可能导致 Bug，所以请在更新后重启主题，或者请仔细检查是否有留空的设置项（这里主要指选择型设置项，文本类设置项似乎没这个问题）。

### 站点副标题

该项用以设定首页的标题栏中站点标题后显示的文字。

### 站点 LOGO

该项应为一个图片的 URL 地址，将显示在浏览器顶部标签标题左边。

请勿使用相对地址。

### 站点头像

该项应为一个图片的 URL 地址，将显示在首页大标题上方。

请勿使用相对地址。

### 首页背景图像

该项应为一个图片的 URL 地址，用以设定网站首页背景图片，留空则使用默认紫色渐变背景。

请勿使用相对地址。

### 随机背景图像地址

该项应为一个或多个图片的 URL 地址，用以设定网站文章页、独立页面以及其他页面的头图，设定后将从给定的图片中随机抽取一个显示，留空则使用默认紫色渐变背景。

URL 之间用换行隔开，即每行一个 URL，**请勿包含多余字符**。

请勿使用相对地址。

### 背景气泡

该项用以选择是否在首页以及文章页顶部背景处显示半透明气泡。

### 页脚左下角文字

该项用以设定页脚左下角的说明文字，如 Copyright 和 备案信息。

可添加 HTML 代码以实现更丰富的功能，如跳转链接等。

### 页脚小工具

该项用以选择是否在页面底部显示“最新评论”、“最新文章”和“近期归档”。

### 自定义 css

该项用以提供自定义 css 接口，用户可以填入自己需要的 css 代码来改变主题外观，例如更改字体大小。

自定义 css 的生效不需要清空缓存。

### 全站 pjax 模式

该项用以选择是否启用全站 pjax 模式提升用户访问体验。

请注意：开启该功能后可能会导致站点一些功能不正常，例如如果您未使用主题自带数学公式渲染，而是选择使用其他插件实现该功能，则会导致无刷新打开页面时数学公式插件不工作，因此请仔细检查后决定是否开启该模式。

如果您发现部分功能确实出现了问题，而您又希望开启该模式，则请查看“pjax 回调代码”一项的说明。

### pjax 回调代码

该项用以设定 pjax 渲染完毕后需执行的 JS 代码，以此解决上一项中提到的插件不工作之类的问题。

例如您有一个叫做`myFunction()`的函数在其他插件中调用了，但您发现它在全站 pjax 模式下不工作，则您应该在该项中填入以下内容：

```js
myFunction();
```

那么在 pjax 执行完毕之后会调用`myFunction()`，问题就解决了。

### katex 数学公式渲染

该项用以选择是否启用 katex 数学公式渲染。

### prism.js 代码高亮

该项用以选择是否启用 prism.js 代码高亮。

### prism.js 行号显示

该项用以选择代码高亮是否显示行号。

### prism.js 高亮主题

该项用以选择 prism.js 代码高亮的主题配色。

### TOC 文章目录

该项用以选择是否启用 TOC 文章目录功能。

启用后将在文章页右侧显示一个可展开和关闭的 TOC 目录。

### TOC 目录展开状态

该项用以选择 TOC 目录栏是否默认展开。

## 短代码

*注意：若无法正常使用此功能，请尝试关闭第三方插件，如第三方文章编辑器。*

### 高亮代码框

标签名：

+ `bbcode`：高亮代码框标签

语法：

```html
<bbcode type="颜色类型">代码框内容</bbcode>
```

示例：

```html
<bbcode type="success">这是绿色高亮代码框，用以显示推荐信息</bbcode>
<bbcode type="danger">这是红色高亮代码框，用以显示警告信息</bbcode>
<bbcode type="warning">这是橙色高亮代码框，用以显示注意信息</bbcode>
<bbcode type="secondary">这是灰色高亮代码框，用以显示引用信息</bbcode>
<bbcode type="info">这是蓝绿色高亮代码框，用以显示高亮信息</bbcode>
<bbcode type="default">这是深蓝色高亮代码框，用以显示高亮信息</bbcode>
<bbcode type="primary">这是紫色高亮代码框，用以显示高亮信息</bbcode>
```

效果：

![bbcode.png](https://i.loli.net/2020/04/07/VEk37bUuXc1lyf6.png)

### 友链

标签名：

+ `bblist`：友链列表标签
+ `bblink`：友链项标签

语法：

```html
<bblist>
<bblink link="友链 URL" icon="友链图标 URL" des="友链描述">友链名称</bblink>
</bblist>
```

示例：

```html
<bblist>
<bblink link="https://tntofu.com" icon="https://tntofu.com/usr/uploads/2020/03/4228973783.jpg" des="三硝基豆腐的博客">豆腐蒸锅</bblink>
<bblink link="https://blog.boxpaper.club" icon="https://tntofu.com/usr/uploads/2020/04/2709766458.png" des="/ No Result !">Rorical</bblink>
</bblist>
```

效果：

![bblink.png](https://i.loli.net/2020/04/07/13ZtBldaNuxqrch.png)

# 截图

![screenshot.jpg](./screenshot.jpg)

# License

Open sourced under the MIT license.

# 其他

+ 主题由[三硝基豆腐](https://github.com/trinitrotofu)、[Rorical](https://github.com/Liupaperbox)和[Totorato](https://github.com/totorato)三人共同完成
+ 基于[Argon Design System](https://www.creative-tim.com/product/argon-design-system)
+ 评论模块中部分代码参照了 Typecho 官方主题 Default
+ Rorical 的 Rorical 主题（同样基于 argon design system）：[https://github.com/Liupaperbox/Rorical](https://github.com/Rorical/Rorical)
+ Totorator 的修改版 Bubble 主题：[https://github.com/totorato/Bubble](https://github.com/totorato/Bubble)

# 更新历史

## 4.0.1

+ 修复了副标题显示不正确的问题（于是 4.0.0 只存活了不到一个小时）

## 4.0.0

+ 更改页面布局为卡片式布局
+ 新增自动更新功能
+ 新增 TOC 目录功能
+ 新增 viewer.js 图片查看器（点击放大）
+ 新增回到顶部按钮
+ 新增副标题设置功能


## 3.0.3

+ 优化 pjax 进度条显示
+ 添加图片圆角
+ 修改高分辨率内容卡片边距
+ 美化搜索框

## 3.0.2

+ 调整首页壁纸全屏显示以美化高分屏显示效果
+ 首页翻页自动滚动至文章列表

## 3.0.1

+ 修复评论卡托条问题
+ 修复左上角标题颜色问题

## 3.0.0

+ 新增 pjax 支持、ajax 评论无刷新及其部分细节优化
+ 新增 KaTeX 数学公式渲染
+ 新增 prism.js 代码高亮
+ 新增短代码功能（高亮代码框以及友链功能）
+ 使用 jsdelivr CDN 加速静态文件加载
+ 更新部分页面布局
+ 文章列表采用分页导航栏代替翻页按钮
+ 修正评论区头像被挤压的问题
+ 修正评论卡由于采用 flex 而高度塌缩的问题

注：此次更新主要由 Rorical 贡献代码，十分感谢

## 2.3.0

+ 支持自定义首页背景图像和其他页面标题栏背景图像随机显示
+ 调整页面按钮样式
+ 评论区布局调整
+ 新增首页头像旋转特效
+ 调整修复部分页面布局以及样式错误
+ 更新截图

## 2.2.2

+ 调整内容页宽度
+ 支持自定义页脚说明文字

## 2.2.1

+ 修复分类显示 Bug(issue #2)
+ 规整代码

## 2.2

+ 优化内容宽度设定
+ 更新换行规则，避免某单词或网址过长导致

## 2.1

+ 页脚显示“最新评论”、“最新文章”和“文章归档”
+ 新增后下角快捷编辑按钮（需登录后显示），方便快速进入后台、编辑文章

## 2.0

+ 采用卡片式页面，提升美观性
+ 美化顶部导航栏样式
+ 新增后台设置 Logo 和 首页头像功能
+ 美化文章列表和文章阅读页中文章状态标签（如分类、作者等）
+ 美化评论区显示，添加博主标志，调整头像大小，提升布局美观性，解决评论卡片无法显示于子评论下方的问题，适配移动端，提升阅读舒适度
+ 采用 font awesome 代替 nucleo 图标集，丰富图标种类
+ 美化加密文章密码表单
+ 调整隐藏/加密文章的评论卡显示机制
+ 调整页面 title 显示机制

## 2.0 之前

我不记得了，也懒得看
