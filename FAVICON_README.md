# CRM 系统 Favicon 图标

## 设计理念

### 视觉元素
- **主色调**：品牌蓝 `#1677ff`（Ant Design 标准蓝）
- **核心图形**：字母 **C** 代表 **CRM**（Customer Relationship Management）
- **内部三点**：象征客户、关系、管理三个核心概念
- **连接线**：代表客户间的关联网络和管理流程

### 寓意
- **C 形**：开放、包容、连接
- **三点**：客户为中心、关系为纽带、管理为手段
- **蓝色**：专业、科技、可信赖

## 文件清单

| 文件 | 格式 | 尺寸 | 用途 |
|------|------|------|------|
| `favicon.svg` | SVG | 32x32 | 现代浏览器标签页图标 |
| `favicon.png` | PNG | 32x32 | 传统浏览器兼容 |
| `logo.svg` | SVG | 64x64 | Apple Touch Icon（移动设备） |

## 技术实现

### 多格式支持
```html
<!-- 现代浏览器优先使用 SVG -->
<link rel="icon" type="image/svg+xml" href="/favicon.svg">

<!-- 传统浏览器使用 PNG -->
<link rel="icon" href="/favicon.png">

<!-- 移动设备使用 Apple Touch Icon -->
<link rel="apple-touch-icon" href="/logo.svg">

<!-- 浏览器主题色 -->
<meta name="theme-color" content="#1677ff">
```

### 浏览器兼容性

✅ **现代浏览器**（Chrome 80+, Firefox 70+, Safari 14+, Edge 80+）
- 使用 SVG 格式，清晰锐利

✅ **传统浏览器**（IE 11, 旧版 Chrome/Firefox）
- 使用 PNG 格式，向后兼容

✅ **移动设备**（iOS Safari, Android Chrome）
- 使用 Apple Touch Icon，添加到主屏幕时显示

## 查看效果

### 本地开发
1. 启动开发服务器：`npm run dev`
2. 访问：http://localhost:8001
3. 查看浏览器标签页图标

### 生产环境
- Netlify 部署后自动生效
- GitHub Pages 部署后自动生效

## 设计规范

### 颜色规范
- **主色**：`#1677ff`（品牌蓝）
- **辅助色**：`#ffffff`（纯白）
- **透明度**：0.95（连接点）

### 尺寸规范
- **基础尺寸**：32x32px
- **最小识别尺寸**：16x16px
- **推荐尺寸**：64x64px（Retina 屏幕）

### 安全区域
- 边缘留白：1px
- 图形主体：居中
- 最小线宽：2px

## 更新记录

### v1.0 - 2026-03-25
- ✅ 初始版本发布
- ✅ SVG + PNG 双格式支持
- ✅ 移动设备兼容
- ✅ 浏览器主题色配置

## 相关文件

- `project/crm-frontend/public/favicon.svg` - SVG 图标
- `project/crm-frontend/public/favicon.png` - PNG 图标
- `project/crm-frontend/public/logo.svg` - Apple Touch Icon
- `project/crm-frontend/index.html` - HTML 引用配置

## 使用示例

### 在 HTML 中使用
```html
<head>
  <link rel="icon" type="image/svg+xml" href="/favicon.svg">
  <link rel="icon" href="/favicon.png">
  <link rel="apple-touch-icon" href="/logo.svg">
  <meta name="theme-color" content="#1677ff">
</head>
```

### 在 Vue 组件中使用
```vue
<template>
  <img src="/favicon.svg" alt="CRM Logo" />
</template>
```

## 注意事项

1. **不要删除源文件**：保持 SVG 和 PNG 两种格式
2. **更新需同步**：修改图标时需同时更新所有格式
3. **缓存问题**：更新后可能需要清除浏览器缓存
4. **尺寸比例**：保持 1:1 正方形比例

## 技术支持

如需修改或重新生成，可参考：
- SVG 源文件可直接编辑
- PNG 可通过 Python 脚本生成
- 在线工具：realfavicongenerator.net
