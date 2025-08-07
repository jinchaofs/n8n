# n8n 科技感紫色主题 - 设计系统更新

## 🎨 修改内容

只修改了 `_primitives.scss` 文件中的两个核心颜色值，让现有的所有组件自动应用科技感紫色主题。

### 修改的变量

**主色调 (Primary Color):**
```scss
// 修改前 - 橙红色
--prim-color-primary-h: 7;        // 橙红色色调
--prim-color-primary-s: 100%;     // 饱和度
--prim-color-primary-l: 68%;      // 明度

// 修改后 - 科技感紫色  
--prim-color-primary-h: 263;      // 紫色色调
--prim-color-primary-s: 70%;      // 饱和度
--prim-color-primary-l: 56%;      // 明度
```

**次要色调 (Secondary Color):**
```scss
// 修改前
--prim-color-secondary-h: 247;    // 蓝紫色
--prim-color-secondary-s: 49%;
--prim-color-secondary-l: 53%;

// 修改后 - 深紫蓝色，与主色调更协调
--prim-color-secondary-h: 240;    // 深紫蓝色
--prim-color-secondary-s: 60%;
--prim-color-secondary-l: 50%;
```

## ✅ 自动生效的组件

由于现有的设计系统使用了基于 HSL 的颜色计算，修改这两个核心变量后，以下所有组件会自动应用新的紫色主题：

- **按钮组件**: 主要按钮、次要按钮、链接按钮等
- **输入框**: 聚焦边框、验证状态等  
- **导航菜单**: 选中状态、悬停效果
- **标签页**: 激活状态
- **表单控件**: 复选框、单选按钮、开关等
- **状态指示**: 加载状态、通知消息等
- **工作流节点**: 选中边框、连接线等

## 🎯 颜色效果

**新的主色调 (H:263, S:70%, L:56%):**
- 基础色: `#7c3aed` - 科技感紫色
- 自动生成的变体:
  - 浅色: `--prim-color-primary-tint-*` 
  - 深色: `--prim-color-primary-shade-*`
  - 透明: `--prim-color-primary-alpha-*`

## 🚀 优势

1. **风险最小**: 只修改颜色值，不改变任何组件逻辑
2. **自动应用**: 所有现有组件无需修改即可应用新主题  
3. **一致性保证**: 基于现有的颜色系统确保视觉一致性
4. **向后兼容**: 可以随时回滚到原来的颜色值

## 🔄 如何回滚

如果需要回滚到原来的橙红色主题，只需将 `_primitives.scss` 中的值改回：

```scss
--prim-color-primary-h: 7;
--prim-color-primary-s: 100%;  
--prim-color-primary-l: 68%;

--prim-color-secondary-h: 247;
--prim-color-secondary-s: 49%;
--prim-color-secondary-l: 53%;
```

这是最简单、最安全的主题修改方式，符合现有设计系统的架构理念。