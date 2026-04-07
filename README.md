# AI 聊天机器人项目

## 项目简介

这是一个基于Spring Boot后端和Vue3前端的AI聊天机器人项目，支持智能对话、客服功能和网络搜索等特性。

## 技术栈

### 后端 (ai-robot-springboot)
- **框架**: Spring Boot
- **数据库**: MyBatis Plus
- **AI集成**: ChatGPT API
- **网络请求**: OkHttp
- **异步处理**: Spring Async
- **日志**: Log4j2

### 前端 (ai-robot-vue3)
- **框架**: Vue 3
- **构建工具**: Vite
- **UI组件**: 自定义组件
- **HTTP客户端**: Axios
- **状态管理**: Pinia (stores)

## 项目结构

```
AI-Chatbot/
├── ai-robot-springboot/          # Spring Boot后端项目
│   ├── src/main/java/com/quanxiaoha/ai/robot/
│   │   ├── advisor/              # 顾问类 (聊天记忆、网络搜索等)
│   │   ├── aspect/               # AOP切面 (操作日志)
│   │   ├── config/               # 配置类
│   │   ├── controller/           # REST控制器
│   │   ├── domain/               # 领域对象
│   │   ├── service/              # 业务服务层
│   │   └── utils/                # 工具类
│   ├── src/main/resources/       # 配置文件
│   └── pom.xml                   # Maven配置
└── ai-robot-vue3/                # Vue3前端项目
    ├── src/
    │   ├── components/           # Vue组件
    │   ├── views/                # 页面视图
    │   ├── stores/               # 状态管理
    │   ├── api/                  # API接口
    │   └── router/               # 路由配置
    ├── public/                   # 静态资源
    └── package.json              # npm配置
```

## 主要功能

- 🤖 **智能对话**: 集成AI模型进行自然语言对话
- 💬 **聊天界面**: 流式渲染Markdown，支持实时对话
- 🔍 **网络搜索**: 集成网络搜索功能增强回答质量
- 📝 **操作日志**: 记录API操作日志
- 👥 **客服功能**: 专门的客服聊天界面
- 🔄 **异步处理**: 支持异步事件处理

## 快速开始

### 后端运行

1. 进入后端目录：
   ```bash
   cd ai-robot-springboot
   ```

2. 配置数据库和AI API密钥：
   - 编辑 `src/main/resources/application.yml`
   - 配置数据库连接
   - 设置ChatGPT API密钥

3. 运行项目：
   ```bash
   mvn spring-boot:run
   ```

### 前端运行

1. 进入前端目录：
   ```bash
   cd ai-robot-vue3
   ```

2. 安装依赖：
   ```bash
   npm install
   ```

3. 启动开发服务器：
   ```bash
   npm run dev
   ```

4. 访问 http://localhost:5173

## 配置说明

### 环境配置
- `application-dev.yml`: 开发环境配置
- `application-prod.yml`: 生产环境配置
- `application.yml`: 基础配置

### 重要配置项
- 数据库连接信息
- ChatGPT API配置
- 线程池配置
- CORS跨域配置

## API接口

### 聊天接口
- `POST /api/chat/stream`: 流式聊天接口
- `POST /api/customer-service/chat`: 客服聊天接口

### 其他接口
- 具体接口请参考控制器代码中的注释

## 开发指南

### 后端开发
- 使用Spring Boot标准开发模式
- 遵循RESTful API设计原则
- 使用MyBatis Plus进行数据库操作
- 利用AOP进行日志记录

### 前端开发
- 使用Vue 3 Composition API
- 组件化开发
- 使用Pinia进行状态管理
- 支持Markdown渲染

## 部署说明

1. 构建后端：
   ```bash
   cd ai-robot-springboot
   mvn clean package
   ```

2. 构建前端：
   ```bash
   cd ai-robot-vue3
   npm run build
   ```

3. 部署到服务器：
   - 后端Jar包部署
   - 前端dist目录部署到Web服务器

## 贡献指南

1. Fork项目
2. 创建特性分支
3. 提交更改
4. 推送分支
5. 创建Pull Request

## 许可证

本项目采用MIT许可证。

## 联系方式

如有问题或建议，请通过GitHub Issues联系。