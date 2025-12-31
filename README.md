# Berry Vite React TypeScript Admin Template

<div align="center">

一个基于 React 19、TypeScript 和 Material UI 的现代化管理后台模板

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-19.2-blue)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-blue)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.2-purple)](https://vitejs.dev/)

</div>

## 项目简介

本项目是基于 [Berry Free React Admin Template](https://github.com/codedthemes/berry-free-react-admin-template) 的 TypeScript 迁移版本。项目从原始的 JavaScript 版本迁移而来，类型系统已基本完善。

## 功能特性

- ✨ 现代化 UI 设计，基于 Material UI v7
- 🌓 深色/浅色主题切换
- 📱 完全响应式布局
- 🔧 TypeScript 类型安全
- ⚡ Vite 构建工具，极速开发体验
- 🎨 自定义主题配置（字体、圆角、颜色等）
- 📊 集成 ApexCharts 图表组件
- 🛠️ 代码分割与懒加载
- 🔍 路径别名支持
- 📦 模块化项目结构
- 🧩 丰富的 UI 组件库
- 🎭 Framer Motion 动画效果
- 🔄 SWR 数据获取
- 🚫 无障碍访问支持

## 技术栈

| 技术 | 版本 | 说明 |
|------|------|------|
| React | 19.2.0 | UI 框架 |
| TypeScript | 5.8.3 | 类型安全 |
| Material UI | 7.3.5 | UI 组件库 |
| Vite | 7.2.6 | 构建工具 |
| React Router | 7.9.6 | 路由管理 |
| ApexCharts | 5.3.6 | 图表组件 |
| Framer Motion | 12.23.25 | 动画库 |
| SWR | 2.3.7 | 数据获取 |
| Emotion | 11.14.0 | CSS-in-JS |
| pnpm | 10.5.2 | 包管理器 |

## 快速开始

### 环境要求

- Node.js >= 18.0.0
- pnpm >= 8.0.0

### 安装依赖

```bash
pnpm install
```

### 开发模式

```bash
pnpm dev
```

开发服务器默认运行在 [http://localhost:3000](http://localhost:3000)，会自动在浏览器中打开。

### 构建生产版本

```bash
pnpm build
```

构建产物将输出到 `dist/` 目录。

### 预览生产构建

```bash
pnpm preview
```

### 代码检查和格式化

```bash
# 检查代码
pnpm lint

# 自动修复代码问题
pnpm lint:fix

# 格式化代码
pnpm prettier
```

## 项目结构

```
berry-vite-react-typescript-admin-template/
├── .env                    # 环境变量配置
├── .gitignore              # Git 忽略配置
├── .prettierrc             # Prettier 配置
├── favicon.svg             # 网站图标
├── index.html             # HTML 入口文件
├── LICENSE                 # MIT 许可证
├── package.json            # 项目配置和依赖
├── pnpm-lock.yaml          # pnpm 锁文件
├── README.md               # 项目说明文档
├── tsconfig.json           # TypeScript 配置
├── tsconfig.node.json      # Node TypeScript 配置
└── vite.config.ts          # Vite 构建配置
└── src/
    ├── api/                # API 接口层
    │   └── menu.ts        # 菜单 API
    ├── assets/             # 静态资源
    │   ├── images/        # 图片资源
    │   │   ├── logo.svg
    │   │   ├── logo-dark.svg
    │   │   ├── auth/     # 认证相关图片
    │   │   ├── icons/    # 图标资源
    │   │   └── users/    # 用户头像
    │   └── scss/          # 全局样式
    ├── contexts/          # React Context 上下文
    │   └── ConfigContext.tsx  # 配置上下文
    ├── hooks/             # 自定义 React Hooks
    │   ├── useConfig.ts
    │   ├── useLocalStorage.ts
    │   ├── useMenuCollapse.ts
    │   └── useScriptRef.ts
    ├── layout/            # 布局组件
    │   ├── Customization/ # 主题自定义组件
    │   │   ├── BorderRadius.tsx
    │   │   ├── FontFamily.tsx
    │   │   └── index.tsx
    │   ├── MainLayout/    # 主布局
    │   │   ├── Footer.tsx
    │   │   ├── HorizontalBar.tsx
    │   │   ├── Header/    # 顶部导航
    │   │   ├── LogoSection/ # Logo 区域
    │   │   ├── MenuList/  # 菜单列表
    │   │   ├── Sidebar/   # 侧边栏
    │   │   └── MenuCard/  # 菜单卡片
    │   ├── MinimalLayout/ # 最小布局（用于登录等）
    │   └── NavigationScroll.tsx
    ├── menu-items/        # 菜单配置
    │   ├── dashboard.ts
    │   ├── index.ts
    │   ├── other.ts
    │   ├── pages.ts
    │   └── utilities.ts
    ├── routes/            # 路由配置
    │   ├── AuthenticationRoutes.tsx
    │   ├── ErrorBoundary.tsx
    │   ├── MainRoutes.tsx
    │   └── index.tsx
    ├── store/             # 状态管理
    │   └── constant.ts
    ├── themes/            # 主题系统
    │   ├── custom-shadows.tsx
    │   ├── index.tsx
    │   ├── palette.tsx
    │   ├── typography.tsx
    │   ├── overrides/     # MUI 组件样式覆盖
    │   │   └── [各组件].tsx
    │   └── theme/         # 主题定义
    │       └── default.ts
    ├── ui-component/      # 可复用 UI 组件
    │   ├── cards/         # 卡片组件
    │   │   ├── MainCard.tsx
    │   │   ├── SubCard.tsx
    │   │   ├── TotalIncomeDarkCard.tsx
    │   │   ├── TotalIncomeLightCard.tsx
    │   │   ├── AuthFooter.tsx
    │   │   ├── CardSecondaryAction.tsx
    │   │   └── Skeleton/  # 骨架屏组件
    │   ├── extended/      # 扩展组件
    │   │   ├── Accordion.tsx
    │   │   ├── AnimateButton.tsx
    │   │   ├── AppBar.tsx
    │   │   ├── Avatar.tsx
    │   │   ├── Breadcrumbs.tsx
    │   │   ├── ImageList.tsx
    │   │   ├── Transitions.tsx
    │   │   └── Form/     # 表单组件
    │   ├── third-party/   # 第三方组件封装
    │   │   └── SimpleBar.tsx
    │   ├── Loadable.tsx   # 代码分割加载组件
    │   ├── Loader.tsx     # 加载动画
    │   └── Logo.tsx       # Logo 组件
    ├── utils/             # 工具函数
    │   ├── colorUtils.ts
    │   ├── getImageUrl.ts
    │   └── password-strength.ts
    ├── views/             # 页面组件
    │   ├── dashboard/     # 仪表盘页面
    │   │   └── Default/   # 默认仪表盘
    │   │       ├── index.tsx
    │   │       ├── EarningCard.tsx
    │   │       ├── PopularCard.tsx
    │   │       ├── BajajAreaChartCard.tsx
    │   │       ├── TotalGrowthBarChart.tsx
    │   │       ├── TotalOrderLineChartCard.tsx
    │   │       └── chart-data/ # 图表数据
    │   ├── pages/         # 功能页面
    │   │   ├── auth-forms/      # 认证表单
    │   │   │   ├── AuthLogin.tsx
    │   │   │   └── AuthRegister.tsx
    │   │   └── authentication/  # 认证页面
    │   ├── sample-page/   # 示例页面
    │   └── utilities/     # 工具页面
    │       ├── Color.tsx
    │       ├── Shadow.tsx
    │       └── Typography.tsx
    ├── App.tsx            # 根组件
    ├── config.ts          # 应用配置
    ├── global.d.ts        # 全局类型定义
    ├── index.tsx          # 应用入口
    ├── reportWebVitals.ts # Web 性能指标
    ├── serviceWorker.ts   # Service Worker
    └── vite-env.d.ts      # Vite 环境类型
```

## 核心功能

### 布局系统

- **MainLayout**: 主布局，包含侧边栏、顶部导航和内容区
- **MinimalLayout**: 最小布局，用于登录页等不需要导航的页面
- **Header**: 顶部导航栏，包含搜索、通知、个人中心
- **Sidebar**: 侧边菜单栏，支持折叠和展开
- **Footer**: 页脚组件

### 主题系统

项目支持深色和浅色主题，并提供丰富的自定义选项：

- 主题切换（深色/浅色）
- 字体选择（Inter、Poppins、Roboto）
- 圆角配置
- 主色调自定义

主题配置位于 `src/themes/` 目录：
- `palette.tsx`: 颜色配置
- `typography.tsx`: 字体配置
- `custom-shadows.tsx`: 自定义阴影
- `overrides/`: Material UI 组件样式覆盖

### UI 组件库

#### 卡片组件
- **MainCard**: 主卡片，包含标题和内容区
- **SubCard**: 子卡片
- **TotalIncomeCard**: 收入统计卡片
- **Skeleton**: 骨架屏加载组件

#### 表单组件
- **FormControl**: 表单控件
- **CustomFormControl**: 自定义表单控件
- **FormControlSelect**: 下拉选择器

#### 导航组件
- **Breadcrumbs**: 面包屑导航
- **Tabs**: 标签页
- **Accordion**: 手风琴折叠面板

#### 数据展示
- **ImageList**: 图片列表
- **Avatar**: 头像组件

### 图表组件

基于 ApexCharts 实现的数据可视化组件：

- **BajajAreaChartCard**: 区域图卡片
- **TotalGrowthBarChart**: 总增长柱状图
- **TotalOrderLineChartCard**: 订单趋势折线图

### 认证系统

包含完整的认证相关页面和组件：
- 登录页面 (`Login.tsx`)
- 注册页面 (`Register.tsx`)
- 认证包装器 (`AuthWrapper1.tsx`)
- 认证卡片 (`AuthCardWrapper.tsx`)

## 路径别名

项目配置了以下路径别名，方便导入模块：

```typescript
import { something } from 'assets/*'           // src/assets/*
import { something } from 'contexts/*'         // src/contexts/*
import { something } from 'hooks/*'            // src/hooks/*
import { something } from 'layout/*'           // src/layout/*
import { something } from 'menu-items/*'       // src/menu-items/*
import { something } from 'routes/*'           // src/routes/*
import { something } from 'store/*'            // src/store/*
import { something } from 'themes/*'           // src/themes/*
import { something } from 'ui-component/*'     // src/ui-component/*
import { something } from 'utils/*'            // src/utils/*
import { something } from 'views/*'            // src/views/*
```

## 开发指南

### 添加新页面

1. **创建页面组件**：在 `src/views/` 对应目录下创建页面组件
   ```typescript
   // src/views/my-new-page/index.tsx
   import MainCard from 'ui-component/cards/MainCard';

   const MyNewPage = () => {
     return (
       <MainCard title="新页面">
         <div>页面内容</div>
       </MainCard>
     );
   };

   export default MyNewPage;
   ```

2. **添加路由配置**：在 `src/routes/` 中添加路由
   ```typescript
   // src/routes/MainRoutes.tsx
   const MainRoutes = {
     path: '/',
     element: <MainLayout />,
     children: [
       {
         path: '/my-new-page',
         element: <Loadable(lazy(() => import('views/my-new-page')) />
       }
     ]
   };
   ```

3. **添加菜单项**：在 `src/menu-items/` 中添加菜单配置
   ```typescript
   // src/menu-items/dashboard.ts
   {
     id: 'my-new-page',
     title: '新页面',
     type: 'item',
     url: '/my-new-page',
     icon: IconsTable,
     breadcrumbs: true
   }
   ```

### 添加新组件

1. 在 `src/ui-component/` 或 `src/ui-component/extended/` 下创建组件
2. 使用 TypeScript 定义 Props 类型
3. 遵循现有的组件结构和命名规范

示例：
```typescript
import { FC, ReactNode } from 'react';

interface MyComponentProps {
  title: string;
  children?: ReactNode;
}

const MyComponent: FC<MyComponentProps> = ({ title, children }) => {
  return <div>{title}{children}</div>;
};

export default MyComponent;
```

### 主题自定义

#### 修改颜色
编辑 `src/themes/palette.tsx`:
```typescript
const palette = (theme: Theme) => ({
  primary: {
    main: '#2296f3',
    // ...
  },
  // ...
});
```

#### 修改组件样式
在 `src/themes/overrides/` 对应文件中覆盖样式：
```typescript
// src/themes/overrides/Button.tsx
const Button = (theme: Theme) => ({
  MuiButton: {
    styleOverrides: {
      root: {
        borderRadius: 8,
      }
    }
  }
});
```

#### 修改主题配置
编辑 `src/themes/theme/default.ts`:
```typescript
const themeCustomizations = {
  borderRadius: 12,
  fontFamily: "'Inter', sans-serif",
  // ...
};
```

## 构建配置

### Vite 配置

项目使用 Vite 作为构建工具，配置位于 `vite.config.ts`：

- 开发服务器端口：3000
- 自动打开浏览器
- 支持主机访问
- 代码分割警告限制：1600KB
- 全局变量定义

### TypeScript 配置

TypeScript 配置位于 `tsconfig.json`：

- 目标版本：ES2020
- 模块系统：ESNext
- 路径别名配置
- JSX 模式：react-jsx

## 浏览器支持

| 浏览器 | 支持版本 |
|--------|----------|
| Chrome | 最新版 |
| Edge | 最新版 |
| Firefox | 最新版 |
| Safari | 最新版 |
| Opera | 最新版 |

## 相关资源

- [Berry 官方文档](https://codedthemes.gitbook.io/berry/)
- [Material UI 文档](https://mui.com/)
- [Vite 文档](https://vitejs.dev/)
- [React 文档](https://react.dev/)
- [TypeScript 文档](https://www.typescriptlang.org/)
- [ApexCharts 文档](https://apexcharts.com/)

## 常见问题

### 1. 依赖安装失败

确保使用 pnpm 作为包管理器：
```bash
pnpm install
```

### 2. 端口被占用

修改 `vite.config.ts` 中的端口配置：
```typescript
server: {
  port: 3001,  // 修改为其他端口
}
```

### 3. TypeScript 类型错误

确保已安装所有类型定义包：
```bash
pnpm install @types/react @types/react-dom
```

## 性能优化

- ✅ 代码分割和懒加载
- ✅ 生产环境自动 Tree Shaking
- ✅ 图片资源优化
- ✅ CSS-in-JS 运行时优化
- ✅ 使用 SWR 进行数据缓存

## 许可证

本项目基于 [MIT License](LICENSE) 开源。

## 作者

**ChuranNeko**

- GitHub: [ChuranNeko](https://github.com/ChuranNeko)
- 仓库: [berry-vite-react-typescript-admin-template](https://github.com/ChuranNeko/berry-vite-react-typescript-admin-template)

## 致谢

本项目基于 [Berry Free React Admin Template](https://github.com/codedthemes/berry-free-react-admin-template) 进行 TypeScript 改造和功能增强，感谢 [CodedThemes](https://github.com/codedthemes) 提供的优秀模板。

## 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 更新日志

### v5.1.0 (TypeScript 迁移版)
- ✅ 从 JavaScript 完整迁移到 TypeScript
- 升级到 React 19.2.0
- 升级到 Material UI 7.3.5
- 升级到 TypeScript 5.8.3
- 升级到 Vite 7.2.6
- 添加 Framer Motion 12.23.25
- 添加 SWR 2.3.7
- 为核心组件添加 TypeScript 类型定义
- 完善全局类型声明
- 配置路径别名支持
- 更新项目文档

---

⭐ 如果这个项目对你有帮助，请给个 Star 支持一下！