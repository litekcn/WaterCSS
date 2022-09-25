# 组件

> 本文将介绍 LiDesign 设计语言的几项组件与其使用方法，如按钮、文本、导航栏等。您可以在左侧侧边栏中展开目录以快速访问您所需的项目。

组件是 LiUX 的基本组成项目。

## Alert 提示

一个提示框，用于提醒用户。

**使用**

需创建一个类名是`liux-alert` 的`div`容器，`liux-alert-primary`类名可以修改颜色，`<span class="liux-alert-icon">`可添加在文字前的图标。

```html
<div class="liux-alert liux-alert-primary">你好！</div>
<div class="liux-alert"><span class="liux-alert-icon">❤</span>我永远爱着你。</div>
```

## Button 按钮

通过点触的方式，执行预设的命令。一个最常见的组件。

**使用**

需要声明`liux-btn`类名。<br>
`liux-btn-primary`类名替换为其他颜色。<br>
`liux-btn-outline `类名设置为线性按钮。`liux-btn-text`类名设置为文字按钮。<br>
更改`liux-btn-xs`（极小）`liux-btn-sm`（小） `liux-btn-md` （中）`liux-btn-lg` （大）`liux-btn-xl`（极大）类名改变按钮大小。<br>
更改`liux-btn-square`（方形）`liux-btn-default`（圆角） `liux-btn-round` （圆形）`liux-btn-block`（方圆）类名改变按钮形状。<br>
添加`disabled`属性禁用该按钮。<br>

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

## Button Group 按钮组

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

## Breadcrumb 面包屑

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

## Card 卡片

一只小卡片，里面集成着内容，就像名片一样，可以包含姓名等。

**使用**

需创建一个类名是`liux-card`的`div`容器，它有两种尺寸，您可以添加`liux-card-hover`（大）`liux-card-flat`（小）修改它。<br>
其中可以设立`header`头部容器，可摆放封面、标题。<br>
在`header`头部容器后，您还可以创建`body`身体容器，可摆放您需要的内容，如产品介绍、自我描述等。<br>
紧接着`body`身体容器，您又能设立`foot`尾部容器，可摆放如按钮、版权等内容。
下方的示例将`header`头部容器作为封面使用，`body`身体容器做标题、介绍使用，`foot`尾部容器作为按钮使用。

```html
<!-- 大 -->
<div class="liux-card liux-card-hover">
     <div class="liux-card-header">
          <img src="images/he/he-keyboard.png">
     </div>
     <div class="liux-card-body">何™自动键盘</div>
     <div class="liux-card-footer">
          <button class="liux-btn liux-btn-primary liux-btn-text">Buy it in CyberLitang.com</button>
                </div>
</div>
<!-- 小 -->
<div class="liux-card liux-card-flat">
                <div class="liux-card-body">海洋游是一家伟大的公司。它开创了二次元的新纪元。那就是泄露。泄露的行为令小公司米哈游追悔莫及。</div>
                <div class="liux-card-footer">
                  <button class="liux-btn liux-btn-primary liux-btn-text">View OceanYo Official Page</button>
                </div>
              </div>
```

## Dialog 弹窗

弹出窗口为一个类似于卡片的界面。

**使用**

需创建一个类名是`liux-dialog`的`dialog`容器。<br>
其中可以设立`header`头部容器，可摆放封面、标题。<br>
在`header`头部容器后，您还可以创建`body`身体容器，可摆放您需要的内容，如产品介绍、自我描述等。<br>
紧接着`body`身体容器，您又能设立`foot`尾部容器，可摆放如按钮、版权等内容。
下方的示例将`header`头部容器作为标题使用，`body`身体容器做标题、介绍使用，`foot`尾部容器作为按钮组使用。

```html
<dialog class="liux-dialog" id="wuJianhao">
            <div class="liux-dialog-header">
              <h1 class="liux-dialog-header-title">Wu Jianhao</h1>
            </div>
            <div class="liux-dialog-body">
              Hello, my name's Wu Jianhao, I'm liveing Hubei Suizhou City, Work in Suizhou technology senior high school, and I like 200TB server DDoS! I'm create grasscutter free group~
            </div>
            <div class="liux-dialog-footer">
              <div class="liux-dialog-footer-group">
                <form method="dialog">
                  <button class="liux-btn liux-btn-secondary liux-btn-text" onclick="wuJianhao.close()">You re right</button>
                  <button class="liux-btn" type="submit">Nice to meet you</button>
                </form>
              </div>
            </div>
</dialog>
```
## Dropdown 下拉菜单

可以通过触发，展开菜单的组件。

**使用**

需创建一个类名是`liux-dropdown`的`span`容器。<br>
在按钮中添加`liux-dropdown-trigger`类名，作为打开下拉菜单的入口。<br>
新建类名为`liux-dropdown-menu`的`ul`无序列表，下拉菜单中的项目用`li`列表标签。<br>
添加`liux-dropdown-menu-header`类名，可作为小字指示显示；添加`liux-dropdown-menu-divider`类名，可新建一个水平线，以区分菜单各组；添加`liux-dropdown-menu-divider`类名，成为一个普通的下拉菜单项目。

```html
<span class="liux-dropdown">
            <button class="liux-btn liux-dropdown-trigger">让我看看</button>
            <ul class="liux-dropdown-menu">
              <li class="liux-dropdown-menu-header">腾讯产品合集</li>
              <li class="liux-dropdown-item">小而美</li>
              <li class="liux-dropdown-item">老而坏</li>
              <li class="liux-dropdown-item">小键盘</li>
              <li class="liux-dropdown-item">可爱云</li>
              <li class="liux-dropdown-menu-divider"></li>
              <li class="liux-dropdown-item">注销并卸载</li>
            </ul>
</span>
```

## From 表单

### Input 单行输入框

用户可以在单行输入框上键入内容，和多行输入框不同的是，单行输入框一般键入的文本要会少些。

**使用**

需创建一个类名是`liux-form-input`的`input`输入框，`liux-form-input-md`类名用以修改输入框大小，但`placeholder="md"`属性也要修改一致，与其他控件一样，添加`disabled`属性以禁用，其他可以参考 html 中 input 的属性文档，如改为密码、默认字符等。

```html
<input class="liux-form-input liux-form-input-md" placeholder="md" type="你的密码，没有隐私"/>
```
### Textarea 多行输入框

用户可以在多行输入框上键入内容，但是多行输入框更适用于文本更多的场景。

**使用**

需创建一个类名是`liux-form-input`的`textarea`多行输入框，其余属性与类名和 Input 输入框类似，此处不再赘述。

```html
<textarea class="liux-form-input liux-form-input-md" rows="506"></textarea>
```

### Radios 单选框

供用户选择，但是只能选一项。

**使用**

需创建一个类名是`liux-form-radios`的`textarea`多行输入框，属性设为`type="radio"`，需要显示文字则可外层使用`<label>`标签进行嵌套，参考请看下方示例。添加`disabled`属性以禁用。

```html
<label><input class="liux-form-radios" type="radio" name="LiyuxBook" />璃月·矿业·初等考试·单选题</label>
```

### Checks 多选框

供用户选择，但是能选的东西要比 Radios 单选框要多。

**使用**

需创建一个类名是`liux-form-checks`的`input`输入框，属性设为`type="checkbox"`，需要显示文字则可外层使用`<label>`标签进行嵌套，参考请看下方示例。其余属性与类名和 Radios 单选框类似，此处不再赘述。

```html
<label><input class="liux-form-checks" type="checkbox" />璃月·矿业·初等考试·多选题</label>
```

### Range 滑块

可以滑动的方块。

**使用**

```html
<input class="liux-form-range" type="range" />
```

### Select 选择

可以选择一个项目，它与下拉菜单不一样。

**使用**

```html
<select class="liux-form-select">
                <option>小保底歪了</option>
                <option>小保底不歪</option>
                <option>大保底</option>
              </select>
```

### Upload 上传

可以上传文件。

**使用**

```html
<input class="liux-form-upload" type="file" />
```

## Loading 加载

一项加载动画。

**使用**

```html
<span class="liux-loading"></span>
```

## List 列表

一个乐意列出项目的表格。

**使用**

```html
<ul class="liux-list-group">
        <li class="liux-list-item liux-list-item-action liux-list-item-focus">番鼠骗商家</li>
        <li class="liux-list-item liux-list-item-action">Re灸咯</li>
        <li class="liux-list-item liux-list-item-action">资油宵野猪</li>
        <li class="liux-list-item liux-list-item-action">猿肾白啸声</li>
        <li class="liux-list-item liux-list-item-action">黒磕鸡の癫躺</li>
</ul>
```
           
## Typography 排版

有关排版的详细规则，请查看 [标准](design/README.md) 一文。



