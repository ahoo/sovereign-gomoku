# sovereign-gomoku

五子棋 Web 应用，用于 Sovereign-OS 真实场景端到端验收（Epic 21 C-3）。

## 本地启动

```bash
npm install
npm start
# 访问 http://localhost:3000
```

## 环境变量

- `PORT`：服务端口，默认 3000

## 部署结构

- **开发机（rb.edage.cn）**：修改代码 + git commit
- **部署机（kr.edage.cn）**：git pull + npm start，服务运行在 `:3000`
- **代理机（sp.edage.cn）**：traefik 反向代理，`gomoku.edage.cn` → `kr.edage.cn:3000`
