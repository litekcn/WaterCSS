# 组件

> 本文将介绍 LiDesign 设计语言的几项组件与其使用方法，如按钮、文本、导航栏等。

组件是 LiUX 的基本组成项目。

### Button 按钮

通过点触的方式，执行预设的命令。一个最常见的组件。

**使用**

需要声明`liux-btn`类名。

`liux-btn-primary`类名替换为其他颜色。

`liux-btn-outline `类名设置为线性按钮。`liux-btn-text`类名设置为文字按钮。

更改`liux-btn-xs`（极小）`liux-btn-sm`（小） `liux-btn-md` （中）`liux-btn-lg` （大）`liux-btn-xl`（极大）类名改变按钮大小。

更改`liux-btn-square`（方形）`liux-btn-default`（圆角） `liux-btn-round` （圆形）`liux-btn-block`（方圆）类名改变按钮形状。

添加`disabled`属性禁用该按钮。

```html
<!-- 填充按钮 -->
<button class="liux-btn liux-btn-primary">强调按钮</button>
<button class="liux-btn liux-btn-success">竹清按钮</button>
<!-- 线性按钮 -->
<button class="liux-btn liux-btn-primary liux-btn-outline">线性按钮</button>
<!-- 文字按钮 -->
<button class="liux-btn liux-btn-primary liux-btn-text">文字按钮</button>
<!-- 按钮大小 -->
<button class="liux-btn liux-btn-primary liux-btn-xs">极小</button>
<button class="liux-btn liux-btn-primary liux-btn-sm">小</button>
<button class="liux-btn liux-btn-primary liux-btn-md">中</button>
<button class="liux-btn liux-btn-primary liux-btn-lg">大</button>
<button class="liux-btn liux-btn-primary liux-btn-xl">极大</button>
<!-- 按钮形状 -->
<button class="liux-btn liux-btn-primary liux-btn-square">方形</button>
<button class="liux-btn liux-btn-primary liux-btn-default">圆角</button>
<button class="liux-btn liux-btn-primary liux-btn-round">圆形</button>
<button class="liux-btn liux-btn-primary liux-btn-block">方圆</button>
<!-- 禁用按钮 -->
<button class="liux-btn liux-btn-primary" disabled>你点不了我</button>
```

### Button Group 按钮组

一堆按钮聚在一起，适合用于选页与页卡。

**使用**

需创建一个类名是`liux-btn-group` 的`div`容器，再在里面设立`liux-btn`类名的按钮，`liux-btn-group-xs`等类名可以更改大小。
```html
<div class="liux-btn-group">
        <button class="liux-btn liux-btn-active">1</button>
        <button class="liux-btn">2</button>
        <button class="liux-btn">3</button>
</div>

<div class="liux-btn-group liux-btn-group-xs">
        <button class="liux-btn">1</button>
        <button class="liux-btn liux-btn-active">2</button>
        <button class="liux-btn">3</button>
        <button class="liux-btn">4</button>
</div>
```

### Breadcrumb 面包屑

确定用户所在页面的位置，让用户明白他们现在在网站的哪一个地方，也可以快速导航。这个组件会很适合小鸟们使用。

**使用**

需创建一个类名是`liux-breadcrumb` 的`ul`无序列表，再在里面设立`liux-breadcrumb-item`类名的列表。

```html
<ul class="liux-breadcrumb">
        <li class="liux-breadcrumb-item">乐色报纸</li>
        <li class="liux-breadcrumb-item">文学理工馆</li>
        <li class="liux-breadcrumb-item">名人名言</li>
        <li class="liux-breadcrumb-item">王海洋</li>
</ul>
```

### Card 卡片

一只小卡片，里面集成着内容，就像名片一样。

**使用**

需创建一个类名是`liux-card` 的`div`容器，再在里面设立`liux-breadcrumb-item`类名的列表。

```html
<div class="liux-card liux-card-hover">
     <div class="liux-card-header">
          <img src="images/he/he-keyboard.png">
     </div>
     <div class="liux-card-body">何™自动键盘</div>
     <div class="liux-card-footer">
          <button class="liux-btn liux-btn-primary liux-btn-text">Buy it in CyberLitang.com</button>
                </div>
</div>
```

