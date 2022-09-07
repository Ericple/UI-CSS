# UI.css - 用于纯 HTML/CSS/JS 前端开发人员的打包框架

网址：https://peercat.cn/uicss

＃＃ 内容

- [用法](#usage)
- [组件](#components)
    - [按钮](#button)
        - [默认按钮](#default-button)
        - [普通按钮](#normal-button)
        - [危险按钮](#danger-button)
        - [禁用按钮](#disabled-button)
        - [虚线按钮](#dashed-button)
    - [菜单](#menu)
      - [项目]（#项目）
    - [卡片]（#card）
    - [布局](#layout)
        - [头部](#layouthead)
- [函数](#functions)
    - [提示](#uprompt)

＃＃ 用法
> 下载最新版本，将“dist”文件夹中的所有文件添加到您的项目文件夹中，然后添加：

> `<link rel="stylesheet" href="PATH\\TO\\main.css">`

> 到您要构建的 HTML 文件。

---

＃＃ 成分

＃＃＃ **按钮**
UI.css Framework(1.0.0)中定义了5种按钮，
 他们每个人都有自己独特的风格。您应该在不同的场合使用不同类型的按钮。

#### 默认按钮

第一种是“默认”。它只是称为默认值，并不意味着您不需要定义什么样的
按钮它在类列表中。要将“默认按钮”添加到您的 HTML 文件，请添加：
`<button class="default">你想要什么名字</button>`
到您的 HTML 代码。

#### 普通按钮

第二种是“正常”。你也可以称它为'Primary'类型，它对用户更有吸引力，所以你应该使用它
作为您网站中的主要按钮。要在 HTML 文件中添加“普通按钮”，请添加：`<button class="normal">Whatever
你想要的名字</button>`
到您的 HTML 代码。

#### 危险按钮

第三种是“危险”。如果您想向用户传达危险信息，请使用此按钮。例子
包含删除按钮/清除按钮等等。不管它是什么，你知道我的意思。添加“危险按钮”
在您的 HTML 文件中，添加：`<button class="danger">您想要的任何名称</button>`
到您的 HTML 代码。

#### 禁用按钮

第四种是“禁用”，在您将某些按钮设置为“禁用”之前，请删除列表中的其他类名，或者
它会显示不正确。
要添加“禁用”按钮，请在 HTML 代码中添加：`<button class="disabled">任意名称</button>`。

#### 虚线按钮

第五种是'Dashed'，这个按钮和默认按钮的唯一区别是虚线按钮有一个虚线边框，
它没有默认按钮那么有吸引力。要添加“虚线”按钮，请添加：`<button class="dashed">您想要的任何名称
</button>` 添加到您的 HTML 代码中。

---

＃＃＃ **菜单**

该组件用于构建您网站的菜单。

---

＃＃＃ **卡片**

该组件旨在让您向用户显示信息。

＃＃＃ **布局**

此组件可帮助您构建站点结构。

#### 布局.HCF

这个类有一个预设的结构，它包含`Header`/`content`/`footer`。基本上它是一个
网站的经典结构。添加 `<Layout class="HCF"></layout>` 以应用此结构。

 标头具有“对齐”属性。
默认大小是'fit-content'，这意味着如果你不设置它，它不会在有时显示
head 元素中没有内容。您可以将其设置为 `normal` 以将其扩展为 65px，就像这样：
`<header class="head normal"></Layout>`。至于对齐设置，如果你不设置任何东西，它会
向左对齐。添加 `ctal` 将其更改为居中对齐，或添加 `rtal` 更改为右对齐。

---
＃＃ 功能

- ### **立即提出**

**用法**：使用 uprompt 向用户显示消息。为了使它工作，请添加一个元素`<Messages id="Messages">
</Messages>` 添加到您的 HTML 文件中。

**参数**：（类型：数字，消息：字符串，lastTime：数字）

- 类型：定义您要显示的消息类型。有4种类型，1代表成功；
2 指信息； 3指警告； 4 指错误。

**示例**：`uprompt(1,'Hello ui.css!',3)`
