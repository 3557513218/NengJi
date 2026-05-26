# NengJi
能级农场小程序

---

## 项目详细说明与功能

### 小程序端（NengJi）
能级农场小程序，为农场管理和用户交易服务提供前端支持。

### 后端 API（Nengji-Farm-API）
多端支撑（微信小程序、后台、厨房看板）的智慧农场后端，涵盖商品交易、点单、活动预约、用户管理、退款、物流等全链路场景。

#### 技术栈
- .NET 8 (WebAPI) + C# 12
- MySQL 8.0（Entity Framework Core + Pomelo MySQL）
- JWT Bearer 验证，BCrypt 密码加密
- API 文档：Swagger

#### 主要功能
- 商品交易与订单（含微信支付与物流）
- 餐饮扫码点单，厨房订单推送
- 活动管理与预约核销
- 用户&后台管理员体系
- 售后退款
- 一亩田认购、配送排期

#### 安装与运行
```bash
git clone https://github.com/3557513218/NengJi.git
# 如果只需要API端，进入Nengji-Farm-API
# 修改 appsettings.json 填写你的MySQL参数
dotnet ef database update    # 首次使用需迁移数据库
dotnet run                  # 启动API
```
Swagger接口文档访问：`http://localhost:5000/swagger`

#### 项目结构（部分）
```
Nengji-Farm-API/
├── Controllers/    # API 控制器（商品/订单/用户等）
├── Services/       # 业务逻辑层
├── Dtos/           # 数据传输对象
├── Entities/       # 数据库实体
├── Data/           # 数据库上下文
├── Middleware/     # 中间件（异常、认证等）
├── wwwroot/        # 静态资源
```

> 如需更详细API文档、接口说明，可参考 Nengji-Farm-API 文件夹或联系项目维护者。

---

以上内容为自动补全文档，如需修订请随时联系维护者。
