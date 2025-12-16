````plaintext
my-portfolio/
├── _config.yml            # 核心配置文件
├── CNAME                  # 自定义域名文件（后期配置）
├── .nojekyll              # 告诉GitHub不要忽略下划线开头的文件
├── _layouts/              # 页面布局模板
│   ├── default.html       # 全局基础布局 (Head, Header, Footer)
│   ├── home.html          # 主页专用布局
│   └── post.html          # 博客文章专用布局
├── _includes/             # 可复用组件
│   ├── header.html        # 导航栏
│   ├── footer.html        # 页脚
│   └── project-card.html  # 项目卡片组件
├── _posts/                # 博客文章存放处
│   └── 2025-01-01-welcome.md
├── assets/                # 静态资源
│   ├── css/
│   │   └── style.css      # 核心样式表 (使用CSS Variables实现深色模式)
│   ├── js/
│   │   └── main.js        # 交互逻辑
│   └── images/            # 图片资源
├── index.html             # 网站入口
├── about.md               # 关于页面
├── projects.md            # 项目集页面
├── blog.html              # 博客列表页
└── contact.html           # 联系页面
```