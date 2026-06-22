# 布卓 Fashion AI 前端

对外访问前端，用于展示和承载鞋服行业智能体平台。

- 对外前端域名：`https://fashion.buzhuo.media`
- 部署方式：Cloudflare Pages
- 后端 API：`https://api.yuanzhoulv.cloud`
- 后台管理：`https://admin.yuanzhoulv.cloud`

## 本地开发

```bash
npm install
npm run dev
```

## 构建

```bash
npm run build
```

Cloudflare Pages 配置：

- Build command: `npm run build`
- Output directory: `dist`
- Production branch: `main`

## 环境变量

```env
VITE_API_BASE_URL=https://api.yuanzhoulv.cloud
VITE_ADMIN_URL=https://admin.yuanzhoulv.cloud
```
