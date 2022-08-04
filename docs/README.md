# UI.css - Packed Framework For Pure HTML/CSS/JS Front-End Developer


## Usage
> download the latest release, add all the files in './dist' folder to your project folder, then add : 

> `<link rel="stylesheet" href="PATH\\TO\\main.css">`

> to the HTML file you want to build.

---

## Components

### **Button**
There are 5 kinds of button defined in the UI.css Framework(1.0.0),
 each of them has its own unique style. You should use different type of button in different occasion.

#### Default Button

The first kind is 'Default'. It is just called default, it doesn't means that you don't need to define what kind of 
button it is in the classList. To add a 'Default button' to your HTML file, add:
`<button class="default">Whatever name you want</button>`
to your HTML code.

#### Normal Button

The second kind is 'Normal'. You can also call it 'Primary' type, it is more attractive for users, so you should use it 
as primary button in your website. To add a 'Normal button' to your HTML file, add: `<button class="normal">Whatever 
name you want</button>`
to your HTML code.

#### Danger Button

The third kind is 'Danger'. If you want to convey a danger information to user, please use this button. Examples 
contains Delete Button/ Clear Button and soooo on. Whatever it will be, you know what I mean. To add a 'Danger button' 
to your HTML file, add: `<button class="danger">Whatever name you want</button>`
to your HTML code.

#### Disabled Button

The forth kind is 'Disabled', before you set some buttons as 'disabled', please remove other classNames in the list, or 
it will display incorrectly.
To add a 'Disabled' Button, add: `<button class="disabled">Whatever name you want</button>` to your HTML code.

#### Dashed Button

The fifth kind is 'Dashed', the only difference between this and default button is dashed button has a dashed border, 
it's less attractive than default button. To add a 'Dashed' Button, add: `<button class="dashed">Whatever name you want
</button>` to your HTML code.

---

### **Menu**

This component is here to build your site's menu.

Example:

```HTML
<div class="menu">

    <a class="item" id="document">Document</a>

    <a class="item" id="publish">Publish</a>

</div>
```

Preview:

![image-20220730214202520](.\image1.png)

#### Secondary Menu

This component allows you to set secondary menu binding to the first one.

**Warning**: To make secondary menu works properly, the parent element must be a 'div'.

Example:
```HTML
<div class="menu">

    <div class="item" id="document">

        Document

        <span>

            <a>Secondary Menu1</a>

            <a>Secondary Menu2</a>

            <a>Secondary Menu3</a>

        </span>

    <a class="item" id="publish">Publish</a>

</div>

```


Preview:

![image-20220730214912415](./image2.png)



---

### **Card**

This component is designed for you to display information to the user.

Example:

```HTML
<Card class="default">
    <t><!--PLACE YOUR TITLE HERE--></t>
    <tc><!--PLACE YOUR CONTENT HERE--></tc>
    <tc><!--PLACE YOUR CONTENT HERE--></tc>
    <tc><!--PLACE YOUR CONTENT HERE--></tc>
</Card>
```



### **Layout**

This component is here to help you build your site's structure.

Example 
```HTML
<Layout class="HCF">
    <header class="normal rtal">
        <!--PLACE LOGO/MENU/SEARCHBOX OR SOMETHING ELSE HERE-->
    </header>
    <content>
        <!--PLACE YOUR WEB CONTENT HERE-->
        <div><h1>Hello world!</h1></div>
        <!--EVERY SINGLE ELEMENT MUST BE WARPED BY A DIV-->
    </content>
    <footer>
        <!--FOR USERS IN CHINA MAINLAND, PLACE YOUR IPC AUTHORIZE CODE AND OTHER THINGS HERE-->
    </footer>
</Layout>
```

#### class [HCF]

The HCF class provides a template with a header/content/footer. It is well designed for you to show almost everything to user.

Example: `<Layout class="HCF"></Layout>`

---
## Functions

- ### **uprompt**

**usage**: use uprompt to display a message to user. To make it works, please add an element `<Messages id="Messages">
</Messages>` to your HTML file.

**parameters**:(Type:number, message:string, lastTime:number)

- Type: Defines what kind of message you want to show. There are 4 kinds of type, 1 refers to success;
2 refers to info; 3 refers to warning; 4 refers to error.

**example**:
```Javascript
uprompt(1,'Hello ui.css!',3);
//THIS CODE WILL DISPLAY A SUCCESS MESSAGE WRITEN "Hello ui.css!" AND LAST FOR 3 SECONDS.
```

---

## CUSTOM ELEMENTS

A well-designed website must have some special rules. To bring the best experience to users, I've designed
these custom elements.

### `<endc></endc>`

endc Refers to "The End Character". It is specially designed for some language like Chinese. When there's a
word at the end of the line, it must be combined but not being departed, so please warp it using `<endc>`

Example:
```HTML
<p>
    这是一段话，但是当浏览器被缩放时，最后一个词有可能被折叠。为防止这种情况，请使用"endc"标签将最后的词汇包围，以为用户阅读提供最佳的
    <endc>视觉体验！</endc>
</p>
```

### `<Messages></Messages>`

Messages is a function required element. uprompt uses it to place `<Message></Message>` element.