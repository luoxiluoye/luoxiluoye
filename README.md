# 英文文献阅读器（含后端代理）

## 1) 启动后端代理（保护 API Key）

```bash
npm install
cp .env.example .env
# 编辑 .env，填入 OPENAI_API_KEY
npm start
```

启动后默认地址：`http://localhost:8787`。

健康检查：`GET /health`

代理接口：`POST /api/chat/completions`

## 2) 打开前端页面

直接打开 `英文文献阅读器.html`，或使用静态服务器：

```bash
python -m http.server 8000
```

页面里选择：
- 连接方式：`后端代理（推荐）`
- 代理地址：`http://localhost:8787/api/chat/completions`

即可在浏览器中不暴露 OpenAI Key。
