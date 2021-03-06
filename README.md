# Antd Admin

[![React Native](https://img.shields.io/badge/react-^15.4.1-brightgreen.svg?style=flat-square)](https://github.com/facebook/react)
[![Ant Design](https://img.shields.io/badge/ant--design-^2.7.3-yellowgreen.svg?style=flat-square)](https://github.com/ant-design/ant-design)
[![dva](https://img.shields.io/badge/dva-^1.1.0-orange.svg?style=flat-square)](https://github.com/dvajs/dva)

[![GitHub issues](https://img.shields.io/github/issues/zuiidea/antd-admin.svg?style=flat-square)](https://github.com/zuiidea/antd-admin)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/zuiidea/antd-admin/pulls)
[![MIT](https://img.shields.io/dub/l/vibe-d.svg?style=flat-square)](http://opensource.org/licenses/MIT)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com)

演示地址 <http://zuiidea.github.io/antd-admin/>

备用地址 <http://47.92.30.98:8000>

## 特性

-   基于[react](https://github.com/facebook/react)，[ant-design](https://github.com/ant-design/ant-design)，[dva](https://github.com/dvajs/dva)，[Mock](https://github.com/nuysoft/Mock) 企业级后台管理系统最佳实践
-   基于[Mock](https://github.com/nuysoft/Mock)实现脱离后端独立开发
-   基于Antd UI 设计语言，提供后台管理系统常见使用场景
-   基于[dva](https://github.com/dvajs/dva)动态加载 Model 和路由，按需加载
-   浅度响应式设计

## 更新日志

### 4.2

`2017-04-28`

-     修改user相关API使用`Restful`风格
-     增加user页面多条件查询[#266](https://github.com/zuiidea/antd-admin/issues/226)
-     修复菜单默认高亮[#201](https://github.com/zuiidea/antd-admin/issues/201)

`2017-04-21`

-     重写Menu，Bread组件及配置文件，[说明](https://github.com/zuiidea/antd-admin/wiki/%E8%8F%9C%E5%8D%95%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)

### 4.1

`2017-04-14`

-   升级开发工具为[roadhog](https://github.com/sorrycc/roadhog)
-   使用`roadhog`的mock功能
-   增强`utils/request.js`跨域处理能力

## 开发构建

### 目录结构

```bash
├── /dist/           # 项目输出目录
├── /src/            # 项目源码目录
│ ├── /components/   # UI组件及UI相关方法
│ │ ├── skin.less    # 全局样式
│ │ └── vars.less    # 全局样式变量
│ ├── /routes/       # 路由组件
│ │ └── app.js       # 路由入口
│ ├── /models/       # 数据模型
│ ├── /services/     # 数据接口
│ ├── /themes/       # 项目样式
│ ├── /mock/         # 数据mock
│ ├── /utils/        # 工具函数
│ │ ├── config.js    # 项目常规配置
│ │ ├── menu.js      # 菜单及面包屑配置
│ │ ├── config.js    # 项目常规配置
│ │ ├── request.js   # 异步请求函数
│ │ └── theme.js     # 项目需要在js中使用到样式变量
│ ├── route.js       # 路由配置
│ ├── index.js       # 入口文件
│ └── index.html     
├── package.json     # 项目信息
├── .eslintrc        # Eslint配置
└── .roadhogrc.js    # roadhog配置
```

文件夹命名说明:

-   components：组件（方法）为单位以文件夹保存，文件夹名组件首字母大写（如`DataTable`），方法首字母小写（如`layer`）,文件夹内主文件与文件夹同名，多文件以`index.js`导出对象（如`./src/components/Layout`）
-   routes：页面为单位以文件夹保存，文件夹名首字母小写（特殊除外，如`UIElement`）,文件夹内主文件以`index.js`导出，多文件时可建立`components`文件夹（如`./src/routes/dashboard`），如果有子路由，依次按照路由层次建立文件夹（如`./src/routes/UIElement`）

### 快速开始

克隆项目文件:

    git clone https://github.com/zuiidea/antd-admin.git

进入目录安装依赖:

    npm i 或者 yarn install
    npm i roadhog@0.6.0-beta.6 -g

开发：

```bash
npm run dev
打开 http://localhost:8000
```

构建：

```bash
npm run build

将会生成dist目录
```

代码检测：

```bash
npm run lint
```

## 参考

用户列表：<https://github.com/dvajs/dva/tree/master/examples/user-dashboard>

dashboard设计稿：<https://dribbble.com/shots/3108122-Dashboard-Admin> （已征得作者同意）

## 截屏

web

![](assets/demo4.gif)

移动

![](assets/demo3.gif)
