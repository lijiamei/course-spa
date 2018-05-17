# SPA 富应用开发通关任务

## 统一要求

- 创建 spa 项目目录，所有作业放到 spa 目录下
- 在 GitHub 上创建 spa 仓库，将每次课的作业代码推送到 GitHub 仓库上
- GitHub 的 spa 仓库启用 GitHub Pages 功能
- HTML、CSS 和 JavaScript 代码分离
- HTML 文件处理页面的内容，并关联样式文件和代码文件
- CSS 文件处理页面上控件的外观和布局
- JavaScript 文件处理页面交互逻辑

## 第 1 次课：课程简介

### 任务 1：矩形计算器

基本要求：
- 根据输入的矩形的长度和宽度计算矩形的周长和面积
- 使用 H5 内置控件实现
- 解决浮点舍入误差的问题
- 不用考虑数据合法性校验
- 支持科学计数法的数据计算

增强体验：
- 增加网站图标，Chrome 开发者工具的控制台窗口，不要输出错误
- 添加页面初始焦点，初始焦点设置为第一个文本框
- 计算结果文本框不可编辑
- 设备自适应，页面在手机上可以正常显示
- 增加必填字段提示
- 不用考虑数据合法性校验

示例参考：
- [矩形计算器](http://spa.wangding.in/00-first-app/index.html)

## 第 2 次课：H5 内置控件

### 任务 1：定时器按钮

基本要求：
- 使用 H5 内置控件实现
- 按钮初始状态为禁用
- 禁用状态下，点击按钮，不会有任何响应
- 倒计时 6 秒
- 每隔一秒按钮文字显示剩余秒数
- 倒计时结束后，按钮状态为启用
- 启用状态下，点击按钮，会弹出 alert 弹框

示例参考：
- [定时器按钮](http://spa.wangding.in/01-html-widget/04-button.html)

### 任务 2：密码可见

基本要求：
- 使用 H5 内置控件实现
- 在文本框中输入任意字符，并不显示输入的字符，而显示点（隐藏密码）
- 文本框的右侧有眼睛闭合的图标
- 当鼠标移到眼睛图标时
- 密码框中的密码可以正常显示
- 眼睛关闭的图标变成眼睛睁开的图标
- 当鼠标移出眼睛图标时
- 密码框中的密码不可见
- 眼睛睁开的图标变成眼睛闭合的图标
- 密码框设置为初始焦点

示例参考：
- [密码可见](http://spa.wangding.in/01-html-widget/13-password.html)

### 任务 3：范围控件

基本要求：
- 使用 H5 内置控件实现
- 用滑杆控件输入自己的年龄，滑杆的最小值为 0，最大值为 100
- 滑块拖动后，下方显示年龄数据
- 初始滑块位于最左边，下方的年龄数据为 0 岁

示例参考：
- [范围控件](http://spa.wangding.in/01-html-widget/31-range.html)

### 任务 4：进度条控件

基本要求：
- 使用 H5 内置控件实现
- 用进度条控件模拟下载文件的进度
- 进度条控件下方有三个按钮：开始、暂停和重置
- 开始按钮点击后，进度条显示下载进度
- 暂停按钮点击后，下载进度暂停
- 重置按钮点击后，下载进度条恢复初始状态
- 多次点击开始按钮，点击一次暂停按钮，要求进度条能够暂停

示例参考：
- [范围控件](http://spa.wangding.in/01-html-widget/31-range.html)

## 第 3 次课：数据合法性校验

### 任务 1：字段级验证

基本要求：
- 以第一个 web app 矩形计算器的代码为基础
- 对矩形的宽度和高度两个字段进行字段级数据合法性校验
- 对非法数据提供清晰明确的错误提示
- 做以下几个方面的校验：
  - 数据不能为空
  - 数据类型不对，数据不能是字符串，而应该是数字
  - 数据的取值范围错误，宽度和高度都应该大于零
- 初始焦点在宽度文本框上，按 Tab 键时，进行数据合法性校验
- 如果数据不合法，Tab 键不移动到下一个文本框
- 如果宽度和高度是错误的（上面三种错误的任意一种），点击计算按钮（可以点击多次），不应该计算出周长和面积

示例参考：
- [字段级验证](http://spa.wangding.in/02-validation/00-field-validation.html)

### 任务 2：字符级验证

基本要求：
- 在字段级验证的基础上编写字符级验证
- 此代码功能应该具备字段级验证的所有功能，除此之外，还要实现下面的功能
- 合法的字符包括：0~9 是个数字、小数点和科学计数法的 e 和 E
- 非法字符，除了上面合法字符以外的字母和标点符号
- 在矩形的宽度和高度输入框中输入非法字符，非法字符不会出现在文本框中

参考示例：
- [字符级验证](http://spa.wangding.in/02-validation/01-char-validation.html)

### 任务 3：表单级验证

基本要求：
- 对数据合法性校验的方面跟字段级验证相同
- Tab 键进行焦点切换时不进行数据合法性验证
- 键盘输入字符时不对非法字符进行判断，不拦截非法字符
- 只有点击计算按钮时才进行数据合法性校验
- 出现验证错误时，只报告第一个验证的错误
- 只有数据验证都通过之后，才计算矩形的周长和面积

参考示例：
- [表单级验证](http://spa.wangding.in/02-validation/02-form-validation.html)

### 任务 4：H5 验证

基本要求：
- 利用 H5 内置控件提供的数据合法性校验功能
- 实现字段级和字符级数据合法性校验
- 通往 H5 验证的伪类来提供数据验证与否的标记

参考示例：
- [H5 验证](http://spa.wangding.in/02-validation/03-h5-validation.html)

## 第 4 次课：第三方组件

### 任务 1：二进熵函数

基本要求：
- 使用 EChart 组件绘制二进熵函数曲线
- 二进熵函数：`H(p) = -p*log(p)-(1-p)log(1-p)`
- 二进熵函数中 p 是概率，取值范围是 0~1 之间
- 二进熵函数的对数底数是 2

参考资料：
- [EChart 的官方文档](http://echarts.baidu.com/tutorial.html)

示例参考：
- [二进熵函数](http://spa.wangding.in/03-third-party-widget/01-echart.html)

### 任务 2：百度地图

基本要求：
- 展示百度地图
- 百度地图的中心点为河北师大软件学院
- 在地图上标注 505 教室
- 信息窗口中显示课程名字、地点、时间和老师的头像信息

参考资料：
- [百度地图官方网站](http://lbsyun.baidu.com/index.php)
- [百度地图核心类](http://lbsyun.baidu.com/cms/jsapi/reference/jsapi_reference_3_0.html)
- [百度地图示例](http://lbsyun.baidu.com/jsdemo.htm)

示例参考：
- [百度地图](http://spa.wangding.in/03-third-party-widget/04-map.html)

### 任务 3：语法高亮

基本要求：
- 使用 behave 插件让 textarea 文本框具有 IDE 的代码编辑功能
- 点击添加按钮后 textarea 文本框中的代码添加到页面上
- 页面上的代码呈现出语法高亮

参考资料：
- [behave.js](http://jakiestfu.github.io/Behave.js/)
- [highlight.js](https://github.com/isagalaev/highlight.js)

示例参考：
- [语法高亮](http://spa.wangding.in/03-third-party-widget/02-heightlight.html)

### 任务4：Excel 表格

基本要求：
- 使用 handsontable 插件在页面上显示一个 Excel 表格
- 表格提供上下文菜单
- 在页面上显示一个有意义的数据

参考资料：
- [handsontable](https://handsontable.com/)

示例参考：
- [Excel 表格](http://spa.wangding.in/03-third-party-widget/03-excel.html)

### 任务5：数学公式编辑（选做）

基本要求：
- 使用 Mathquill 插件在页面上实现一个数学公式编辑功能
- 通过添加按钮将数学公式编辑框中的数学公式添加到页面上

参考资料：
- [Mathquill](http://docs.mathquill.com/en/latest/)

示例参考：
- [数学公式编辑](http://spa.wangding.in/03-third-party-widget/05-formula.html)

## 第 5 次课：自定义组件（上）

### 任务 1：定时器按钮组件

基本要求：
- 封装定时器按钮组件
- 封装后的代码文件包括：一个 js 文件和一个 css 文件
- 定时器按钮支持两种应用场景
- 场景一：初始状态禁用，倒计时后，按钮启用，启用后按钮可以点击，点击后按钮一直处于启用状态
- 场景二：初始状态启用，点击按钮后，按钮禁用，倒计时，倒计时结束后，按钮启用，循环往复
- 创建定时器按钮时，可以通过参数初始化：
  - container：创建定时器按钮的容器
  - tLength：定时器时长
  - enable：定时器按钮的初始状态
  - title：定时器按钮的文字
- 定时器按钮启用状态，被点击时，暴露 `timer-button-click` 事件
- 编写定时器按钮的测试页面

示例参考：
- [定时器按钮](http://spa.wangding.in/04-ui-component/01-button/09-index.html)

### 任务 2：密码可见组件

基本要求：
- 封装密码可见组件
- 封装后的代码文件包括：一个 js 文件和一个 css 文件
- 创建密码可见组件时，可以通过参数初始化：
  - container: 创建密码可见组件的容器
- 密码可见组件暴露一个 getPwd 方法，返回密码明文
- 编写密码可见组件的测试页面

示例参考：
- [密码可见](http://spa.wangding.in/04-ui-component/02-password/01-index.html)

## 第 6 次课：自定义组件（中）

### 任务 1：定时器按钮

基本要求：
- 在之前封装的定时器按钮组件基础上
- 用 require.js 重新封装定时器按钮
- 修改测试页面，按需加载定时器按钮组件

示例参考：
- [定时器按钮-按需加载](http://spa.wangding.in/04-ui-component/01-button/10-index.html)

## 第 7 次课：自定义组件（下）

基本要求：


## 第 8 次课：MVC 和数据绑定

要求：

## 第 9 次课：数据存储

要求：

## 第 10 次课：多媒体（上）

要求：

## 第 11 次课：多媒体（下）

要求：

## 第 12 次课：自动化构建

要求：