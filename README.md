# 中国濒危动物 3D 交互地图

基于 Three.js 构建的中国濒危动物 3D 交互地图，覆盖 34 个省级行政区、100+ 种濒危物种。

## 功能特性

- 🗺️ **3D 中国地图** - 基于 GeoJSON 的省份多边形挤出，带地形颜色区分
- 🦁 **100+ 濒危物种** - 每个省份 2-4 种，包含名称、拉丁名、保护等级、栖息地、介绍
- 🎮 **交互操作** - 鼠标悬停高亮、点击查看详情、Tab 切换物种、相机飞行动画
- 🐦 **3D 动物模型** - glTF 格式动物模型（火烈鸟、鹳、马、鹦鹉），带骨骼动画
- 🖼️ **AI 生成图片** - 每种动物配有 AI 生成的高清图片
- 🎬 **抖音视频链接** - 点击可直接跳转抖音搜索对应动物的视频资料
- ✨ **后处理特效** - Bloom 光晕、环境光遮蔽
- 📱 **自适应布局** - 支持桌面和移动端

## 技术栈

- **Three.js v0.160.0** - 3D 渲染引擎（ES Module CDN 加载）
- **Express.js** - 轻量级 Node.js 服务器
- **GeoJSON** - 地理数据（来自 DataV）
- **GLTFLoader** - 3D 模型加载
- **EffectComposer** - 后处理管线

## 快速开始

### 本地运行

```bash
# 安装依赖
npm install

# 启动服务
npm start

# 访问 http://localhost:3000
```

### 部署到 Render

1. 将代码推送到 GitHub 仓库
2. 在 [Render](https://render.com) 创建新的 Web Service
3. 连接 GitHub 仓库
4. 设置：
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
   - **Environment**: `Node`
5. 部署完成后即可通过 Render 分配的 URL 访问

## 项目结构

```
china-endangered-map/
├── public/
│   └── index.html      # 主页面（单文件应用）
├── server.js           # Express 服务器
├── package.json        # 项目配置
├── render.yaml         # Render 部署配置
├── .gitignore
└── README.md
```

## 保护等级说明

| 等级 | 含义 | 颜色 |
|------|------|------|
| CR | 极危 (Critically Endangered) | 🔴 红色 |
| EN | 濒危 (Endangered) | 🟠 橙色 |
| VU | 易危 (Vulnerable) | 🟡 黄色 |
| NT | 近危 (Near Threatened) | 🔵 青色 |

## License

MIT
