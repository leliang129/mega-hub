# 云端拾光

一个简洁优雅的个人导航网站，帮助你高效管理和访问常用网站。

## ✨ 特性

- 🎨 **简约设计** - 清新现代的 UI 界面
- 📱 **响应式布局** - 完美适配桌面、平板、手机
- 🔍 **快速搜索** - 按 `/` 唤醒搜索，即时过滤
- 🎯 **分类管理** - 多维度分类，快速定位
- ⚡ **零依赖** - 纯静态页面，加载极速
- 🔧 **配置驱动** - 修改 JSON 即可自定义内容

## 🚀 快速开始

### 本地运行

```bash
# 克隆仓库
git clone https://github.com/leliang129/mega-hub.git

# 进入目录
cd mega-hub

# 使用任意静态服务器运行
# 方法 1: Python
python3 -m http.server 8080

# 方法 2: Node.js
npx serve .

# 方法 3: VS Code Live Server 插件
# 右键 index.html -> Open with Live Server
```

访问 http://localhost:8080

## 📦 部署

### Cloudflare Pages（推荐）

1. 将代码推送到 GitHub
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
3. 进入 **Workers & Pages** → **Create**
4. 选择 **Pages** → **Connect to Git**
5. 选择仓库，构建配置留空
6. 点击 **Deploy**

### 其他平台

同样支持部署到：
- Vercel
- Netlify
- GitHub Pages
- 任何静态文件托管服务

## ⚙️ 自定义配置

编辑 `nav-config.json` 文件即可添加、删除或修改导航项。

### 配置结构

```json
{
  "categories": [
    {
      "id": "分类ID",
      "name": "分类名称",
      "nameEn": "英文名称",
      "icon": "lucide图标名",
      "iconClass": "图标颜色类",
      "items": [
        {
          "title": "网站名称",
          "url": "https://example.com",
          "description": "网站描述",
          "icon": "lucide图标名",
          "color": "颜色名"
        }
      ]
    }
  ]
}
```

### 图标说明

支持三种图标模式：

| 模式 | 字段 | 示例 |
|------|------|------|
| Lucide 图标 | `"icon": "github"` | 通用图标 |
| 自定义 SVG | `"svg": "<svg>...</svg>"` | 品牌图标 |
| 首字母 | `"initial": "N"` | Notion 等 |

### 支持的颜色

`zinc` `red` `orange` `amber` `yellow` `green` `emerald` `teal` `cyan` `sky` `blue` `indigo` `violet` `purple` `pink` `rose`

## 🛠️ 技术栈

- HTML5
- Tailwind CSS (CDN)
- Lucide Icons
- Vanilla JavaScript

## 📄 License

MIT
