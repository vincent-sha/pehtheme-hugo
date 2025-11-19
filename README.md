# Pehtheme Hugo

Pehtheme Hugo 是一个开源的 Hugo 主题，灵感源自 [Material Design v3](https://m3.material.io/)，采用 Tailwind CSS 精心打造。

![Pehtheme Hugo 预览](https://raw.githubusercontent.com/fauzanmy/pehtheme-hugo/main/images/tn.png?raw=true)

## 在线演示

查看在线演示： [Pehtheme Hugo Live Demo](https://pehtheme-hugo.netlify.app/)

## 性能测试

使用 Pehtheme Hugo 构建站点后，可以通过 PageSpeed Insights 测试性能，点击下面的链接运行测试：

[PageSpeed Insights 测试](https://pagespeed.web.dev/analysis/https-pehtheme-hugo-netlify-app/7gv9zedw83?form_factor=mobile)

## 功能亮点

- 使用 Tailwind CSS 构建
- 首页展示精选文章（通过 `feature` 标签控制）
- 水平导航、标签列表
- 无额外 JavaScript 依赖
- 原生 JavaScript 切换按钮
- 双栏博客布局
- 侧边栏包含最新文章列表
- 语义化 HTML
- 侧边栏广告框

## 安装步骤

按照下列流程即可启动 Pehtheme Hugo：

1. 安装 Hugo 并创建新站点，具体参考 [Hugo 快速上手指南](https://gohugo.io/getting-started/quick-start/)。
2. 克隆 Pehtheme Hugo 主题：
   ```bash
   git clone https://github.com/fauzanmy/pehtheme-hugo.git
   ```
3. 将 `exampleSite` 目录中的两个文件夹和一个配置文件复制到项目根目录：
   ```bash
   exampleSite/
   ├── assets/
   ├── content/
   └── hugo.toml
   ```
4. 启动 Hugo 本地服务器：
   ```bash
   hugo server
   ```

## 配置说明

在项目的配置文件（如 `hugo.toml`）中修改或添加以下内容：

```toml
summaryLength = 20 # 约 20 个单词，约等于 160 个字符

[services]
  [services.googleAnalytics]
    id = 'G-MEASUREMENT_ID' # 你的 GA-4 代码

  [services.disqus]
    shortname = 'shortname' # 你的 Disqus shortname

[pagination]
  pagerSize = 10 # 首页分页文章数量
```

### 评论系统（Giscus）

如果希望使用免费 Giscus 取代默认的 Disqus 占位，配置如下：

1. 在配置文件中添加 `[params.comments]`，用从 https://giscus.app 获得的参数替换示例：
   ```toml
   [params.comments]
     provider = 'giscus'
     repo = 'your-org/your-repo'
     repoId = 'MDEwOlJlcG9zaXRvcnkxMjM0NTY3OA=='
     category = 'General'
     categoryId = 'DIC_kwDOA...'
     mapping = 'pathname'
     reactionsEnabled = '1'
     theme = 'preferred_color_scheme'
     lang = 'zh-CN'
   ```
2. 主题会在 `single` 模板的评论区域自动渲染 Giscus partial，无需额外脚本。
3. 使用 `hugo server` 预览页面，确认每篇文章底部的 Giscus `<script>` 成功加载即可看到评论区。

## 自定义主题

1. 确保本机已安装 Node.js。
2. 将 `exampleSite` 中的 Node.js 配置文件复制到项目根：
   ```bash
   exampleSite/
   ├── package.json
   ├── postcss.config.js
   └── tailwind.config.js
   ```
3. 将 `exampleSite/input.css` 复制到项目的 `assets/input.css`。
4. 安装依赖：
   ```bash
   npm install
   ```
5. 启动 Tailwind 开发模式：
   ```bash
   npm run dev
   ```
6. 构建项目：
   ```bash
   npm run build
   ```

## 许可证

Pehtheme Hugo 使用 MIT 协议，详情见 [LICENSE](https://github.com/fauzanmy/pehtheme-hugo/blob/main/LICENSE)。

## Logo 图标

蛋形图标资源：[Bootstrap Icons - Egg Fried](https://icons.getbootstrap.com/icons/egg-fried/)

## 图片来源

在线预览中使用的图片来源：

```
Images resource:
- https://unsplash.com/photos/Smeer5L0tXM
- https://unsplash.com/photos/2q6C5zDJOsg
- https://unsplash.com/photos/UNd3lRKhwSw
- https://unsplash.com/photos/Ed2AELHKYBw
- https://unsplash.com/photos/rTZW4f02zY8
- https://unsplash.com/photos/OtXJhYjbKeg
- https://unsplash.com/photos/ZPP-zP8HYG0
- https://unsplash.com/photos/ydGRmobx5jA
- https://pixabay.com/vectors/email-newsletter-email-marketing-3249062/
```
