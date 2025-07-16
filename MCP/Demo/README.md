# iCSS 渐变效果演示集合

本文件夹包含了基于 [iCSS](https://github.com/chokcoco/iCSS) 技术的各种现代 CSS 渐变效果演示。

## 📁 文件结构

```
Demo/
├── README.md                           # 本说明文档
├── gradient-complex-background.html    # 复杂渐变背景效果
├── gradient-complex-background.css     # 复杂渐变背景样式
├── gradient-complex-background.js      # 复杂渐变背景交互
├── advanced-gradient-effects.html      # 高级渐变效果展示
├── advanced-gradient-effects.css       # 高级渐变效果样式
├── advanced-gradient-effects.js        # 高级渐变效果交互
├── gradient-border-effects.html        # 渐变边框效果展示
├── gradient-border-effects.css         # 渐变边框效果样式
├── gradient-border-effects.js          # 渐变边框效果交互
└── 渐变背景效果说明.md                 # 详细技术说明
```

## 🎨 演示内容

### 1. 复杂渐变背景效果 (`gradient-complex-background.html`)

**技术特点：**
- 基于 iCSS #214 的圆锥渐变动画
- 多层线性渐变波浪效果
- 径向渐变毛玻璃效果
- 渐变镂空边框（iCSS #266）
- 网格渐变背景（iCSS #273）
- 内凹平滑圆角（iCSS #272）

**交互功能：**
- 鼠标跟随 3D 效果
- 动画速度控制
- 主题切换
- 键盘快捷键支持

### 2. 高级渐变效果展示 (`advanced-gradient-effects.html`)

**技术特点：**
- 彩虹渐变效果
- 玻璃态渐变
- 波浪渐变
- 粒子渐变
- 霓虹渐变
- 几何渐变

**交互功能：**
- 动画速度调节
- 颜色强度控制
- 模糊程度调节
- 颜色随机化
- 实时参数控制

### 3. 渐变边框效果展示 (`gradient-border-effects.html`)

**技术特点：**
- 基础渐变边框
- 动画渐变边框
- 多层渐变边框
- 虚线渐变边框
- 发光渐变边框
- 几何渐变边框

**交互功能：**
- 边框宽度调节
- 动画速度控制
- 发光强度调节
- 点击波纹效果
- 3D 悬停效果

## 🚀 快速开始

### 直接打开
双击任意 HTML 文件即可在浏览器中查看效果。

### 本地服务器
```bash
# 使用 Python 启动本地服务器
python -m http.server 8000

# 或使用 Node.js
npx serve .

# 然后访问 http://localhost:8000/Demo/
```

### 在线预览
将文件上传到任意静态网站托管服务即可在线访问。

## ⌨️ 键盘快捷键

所有演示都支持以下快捷键：

- **空格键**: 暂停/播放动画
- **R**: 随机化颜色
- **+/-**: 调节动画速度
- **方向键**: 调节参数（部分演示）

## 🎯 核心技术

### CSS 自定义属性 (@property)
```css
@property --angle {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}
```

### 圆锥渐变 (Conic Gradient)
```css
background: conic-gradient(
  from var(--angle),
  var(--primary-color),
  var(--secondary-color),
  var(--accent-color),
  var(--primary-color)
);
```

### 遮罩技术 (Mask)
```css
-webkit-mask: 
  linear-gradient(#fff 0 0) content-box,
  linear-gradient(#fff 0 0);
-webkit-mask-composite: xor;
```

### 毛玻璃效果 (Backdrop Filter)
```css
backdrop-filter: blur(15px);
background: rgba(255, 255, 255, 0.1);
```

## 📱 响应式设计

所有演示都支持响应式设计：
- 移动端适配
- 触摸设备支持
- 自适应布局
- 性能优化

## 🌐 浏览器兼容性

### 完全支持
- Chrome 85+
- Firefox 80+
- Safari 14+
- Edge 85+

### 部分支持
- `backdrop-filter`: 需要厂商前缀
- `mask-composite`: 需要 `-webkit-` 前缀
- `@property`: Chrome 85+, Firefox 128+

## 🔧 自定义配置

### 修改颜色主题
```css
:root {
  --primary-hue: 280;
  --secondary-hue: 180;
  --accent-hue: 60;
}
```

### 调整动画速度
```css
:root {
  --animation-speed: 1;
  --rotation-duration: calc(20s / var(--animation-speed));
}
```

### 控制效果强度
```css
:root {
  --intensity: 1;
  --blur-amount: 10px;
  --glow-intensity: 30px;
}
```

## 🎨 技术亮点

### 1. 性能优化
- 使用 `requestAnimationFrame` 优化动画
- GPU 加速的 CSS 变换
- 合理的 `will-change` 属性使用
- 节流处理鼠标事件

### 2. 无障碍支持
- 键盘导航支持
- 减少动画偏好支持
- 高对比度支持
- 语义化 HTML 结构

### 3. 现代 CSS 特性
- CSS Grid 布局
- Flexbox 布局
- CSS 自定义属性
- 现代选择器

## 📚 学习资源

- [iCSS GitHub 仓库](https://github.com/chokcoco/iCSS)
- [CSS 渐变技术指南](https://developer.mozilla.org/zh-CN/docs/Web/CSS/gradient)
- [CSS Mask 详解](https://developer.mozilla.org/zh-CN/docs/Web/CSS/mask)
- [CSS 3D 变换](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform)

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这些演示：

1. 报告 Bug
2. 提出新功能建议
3. 改进代码质量
4. 添加新的渐变效果

## 📄 许可证

本项目基于 MIT 许可证开源。

## 🙏 致谢

感谢 [chokcoco/iCSS](https://github.com/chokcoco/iCSS) 项目提供的灵感和技术基础。这是一个非常优秀的 CSS 技术分享项目，包含了大量高质量的 CSS 技巧和实现方案。

---

**享受现代 CSS 的无限可能！** 🎨✨ 