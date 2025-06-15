# 项目介绍：KomeijiHelper 心理咨询平台

**KomeijiHelper** 是一款基于人机交互理念设计的心理咨询服务平台，前后端分离，提供完整的用户、咨询师交互体验。主要功能包括用户注册登录、预约咨询、聊天记录管理等。

- **前端**：使用 Vue.js 框架开发，独立于后端部署；
- **后端**：基于 Spring Boot 框架，使用 MySQL 存储数据，并依赖 Redis 进行缓存加速；
- **仓库结构**：
  - `frontend/`：前端子模块；
  - `backend/`：后端子模块；
  - 主仓库负责整合部署及整体文档维护。

---

## 🚀 使用说明（启动方式）

### 1. 启动后端服务（Spring Boot）

#### 📦 环境准备

- JDK 17+
- Maven 3.6+
- MySQL 5.7+ 或 8+
- Redis（推荐版本：6+）

#### 🛠 修改配置文件（application.yml）

路径示例：`backend/src/main/resources/application.yml`
请修改以下内容：

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/komeiji_db?useSSL=false&useUnicode=true&characterEncoding=UTF-8
    username: root
    password: your_mysql_password

  redis:
    host: localhost
    port: 6379
    password: your_redis_password  # 如果 Redis 无密码可留空
```

#### ▶ 启动方式

```bash
再IDEA中利用Maven安装好必须的库后 可直接运行
```

项目运行后，后端接口默认地址通常为 `http://localhost:8080/`。

---

### 2. 启动前端服务（Vue 项目）

#### 📦 环境准备

- Node.js（建议版本 16+）
- npm 或 yarn

#### ▶ 启动方式

```bash
cd frontend
npm install        # 或 yarn install
npm run dev# 或 yarn serve
```

启动后默认访问地址为：`http://localhost:8081/`

> ⚠️ 注意：请确保前端配置了正确的后端 API 地址（如在 `.env.development` 或 axios 配置文件中）。
