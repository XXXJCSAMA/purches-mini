# 项目结构说明

## 📁 改进后的目录结构

```
purches-mini/
├── 📁 src/                    # 源代码目录
│   ├── 📁 pages/             # uni-app页面组件
│   │   ├── cart/             # 购物车页面
│   │   ├── detail/           # 订单详情页面  
│   │   ├── index/            # 首页
│   │   ├── order/            # 下单页面
│   │   ├── orders/           # 订单管理页面
│   │   └── shop/             # 商店页面
│   ├── 📁 components/        # 公共组件
│   ├── 📁 utils/             # 工具函数
│   │   └── api.js            # API接口封装
│   ├── 📁 stores/            # 状态管理 (Pinia)
│   ├── 📁 constants/         # 常量定义
│   │   ├── api.js            # API相关常量
│   │   └── suppliers.js      # 供应商常量
│   └── 📁 types/             # TypeScript类型定义
├── 📁 web/                   # HTML静态页面 (H5版本)
│   ├── cart.html
│   ├── index.html
│   ├── orders.html
│   ├── products.html
│   └── ...
├── 📁 static/                # 静态资源
│   ├── api.js                # ❌ 已删除 (重复文件)
│   ├── data.json
│   ├── products.json
│   └── 图片资源...
├── 📄 App.vue               # 应用主组件
├── 📄 main.js               # 应用入口
├── 📄 pages.json            # 页面配置
├── 📄 package.json          # 项目依赖
├── 📄 vite.config.js        # 构建配置
└── 📄 .gitignore            # Git忽略文件
```

## ✅ 改进内容

### 1. **文件分类清晰**
- **src/**: 所有源代码集中管理
- **web/**: HTML页面独立存放 
- **static/**: 纯静态资源

### 2. **删除冗余文件**
- ❌ 删除 `test-tabbar.html` (测试文件)
- ❌ 删除 `static/api.js` (重复的API文件)

### 3. **规范化命名**
- 页面标题与路径保持一致
- 文件夹功能明确

### 4. **添加配置文件**
- ✅ `.gitignore` - Git版本控制
- ✅ `src/constants/` - 常量管理

## 📊 对比分析

| 项目 | 改进前 | 改进后 |
|------|--------|--------|
| **根目录文件数** | 15+ | 10 |
| **HTML文件位置** | 根目录混乱 | web/目录集中 |
| **源码组织** | 分散 | src/目录统一 |
| **重复文件** | 存在 | 已清理 |
| **配置文件** | 不完整 | 标准化 |

## 🎯 使用建议

### uni-app开发
主要使用 `src/` 目录下的文件：
- 页面开发：`src/pages/`
- 组件开发：`src/components/`
- API调用：`src/utils/api.js`

### H5静态部署
直接使用 `web/` 目录下的HTML文件

### 数据管理
- 静态数据：`static/data.json`
- 常量配置：`src/constants/`

## 🔄 后续优化建议

1. **状态管理**: 在 `src/stores/` 中添加 Pinia 状态管理
2. **类型安全**: 在 `src/types/` 中添加 TypeScript 类型定义  
3. **组件库**: 在 `src/components/` 中构建可复用组件
4. **环境配置**: 添加 `.env` 文件管理环境变量

现在项目结构更加清晰和专业! 🚀 