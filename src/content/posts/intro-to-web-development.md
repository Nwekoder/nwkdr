---
title: Intro to Web Development
published: 2024-11-10
description: 'Very basic intro to Web Development.'
image: ''
tags: ['Web Development', 'HTML', 'CSS', 'Javascript']
category: 'Tutorial'
draft: false 
lang: 'en'
---

## Requirements

- A code editor (VS Code is recommended)
- Basic knowledge of typing on Laptop/PC
- Basic knowledge of Copy-Pasting
- English to Your Native Language translator (I'm lazy to rewrite this article to other language, tbh)
- ChatGPT Account (I know you would need it)
- Cup of Coffee (or Tea)

## Intro

Website are consist of 3 parts :

- **HTML** for the structure
- **CSS** for the styling and layout
- **Javascript** to make stuff dynamic

### What is HTML?

HTML (HyperText Markup Language) is the structure of the website made up from bunch of tags. Something like `<p>` or `<h1>` is one of them.

Every tag has their own meaning. For example `<p>` is for paragraph, `<h1>` is the biggest heading and `<div>` to contain/wrap multiple "*element*". These tags can also have their own "*attributes*" to override their default behaviour or mostly their appearance visually on the browser later.

#### What is "element" in HTML?

In HTML, there are opening and closing tag. Just take a look at these snippet.

```html
<p class="im-css-class-btw">
    Some Text
</p>
```

- `<p class="im-css-class-btw">` is the opening tag. Because it's a `<p>` tag, you can write "Some Text" to it.
- `class` is the attribute of the tag. For these attribute, the value will be a "*CSS Class*".
- `</p>` is the closing tag.

If you inspect this web page, you might see something far more overwhelming like this :

```html
<div class="w-11/12 mx-auto">
    <h1 class="font-bold text-5xl mb-8">Some Heading</h1>
    <p class="leading-relaxed">I had no idea what is this</p>
</div>
```

If you seeing something like this, it means the `<div>` tag have a child element. In other words "Element in element". You can structure your web page like that, but maybe you shouldn't cause it's a pain in the ass later if you about to learn how to use "*selector*" in plain CSS.

### What is CSS?

CSS (Cascading StyleSheet) is the way to add styling to your HTML. It might be simple and short at first, but trust me it would be exhausting to write the whole file (that's why we moved to TailwindCSS. Although, it's also pain in the ass in other way).

Basic CSS only consist of 3 things :

- #### Selector

What to style on your HTML page. Mostly you will use "*classes*" instead of the tag name, but you can use "*id*" too as well.

- #### Ruleset

Collection of properties that applied to the "*selector*". In other word, "the bracket".

- #### Rule/Property

Stuff that are applied to the element that you want to style.

For better understanding, take a look at these snippet.

```css
p {
    color: cyan;
    background-color: blue;
}
```

- `p` is the **selector**. It means, you want to style all `<p>` tag in your HTML
- `color: red;` and `background-color: blue;` is the **rule/property**. It means you change the text color to `cyan` and the background color to `blue`
- Everything wrapped in `{}` is the **ruleset**

There's other way to style something with CSS and it's by using "*class*" and "*id*". Here are some example :

```css
.im-css-class-btw {
    background-color: blue;
    padding: 4px;
}

#andIAmID {
    background-color: cyan;
    padding: 4px;
}
```

- Class are represent with `.` prefix
- ID are represent with `#` prefix
- Tag are represent with no prefix

I did saying that you can use tag name to style elements in your HTML. Try me :

```html
<header>
    <div>
        <h1>Your assignment</h1>
        <p>Plz give us some styling so we can be pretty like your waifu</p>

        <div>
            <div>
                <h5>We too</h5>
                <p>I want to be sub title for a card</p>
            </div>
            <div>
                <h5>We too</h5>
                <p>Our card should be in pink</p>
            </div>
            <div>
                <h5>We too</h5>
                <p>I'd like to be yellow, plz</p>
            </div>
        </div>
    </div>
</header>
```

I forgot to say that you can use CSS in multiple way.

- #### You can import it externally
```html
<!-- ... -->
<head>
    <!-- ... -->
    <link rel="stylesheet" href="style.css" />
</head>
<!-- ... -->
```
- #### You can use it internally in your HTML
```html
<!-- ... -->
<head>
    <!-- ... -->
    <style>
        p {
            color: cyan;
            background-color: blue;
        }

        .im-css-class-btw {
            background-color: blue;
            padding: 4px;
        }

        #andIAmID {
            background-color: cyan;
            padding: 4px;
        }
    </style>
</head>
<!-- ... -->
```
- #### You can use it inline as attribute
```html
<p style="color: cyan;">
    Yes, I love cyan. And yes, you write the property.
</p>
```


### What is Javascript?

Javascript is a scripting language to add dynamic interaction to your HTML. In simple example, it change stuff on your HTML if you do something in the website. Like if you press a button, what would happen next?

```html
<button>Click Me</button>

<script>
    var button = document.querySelector("button")

    button.onclick = function() {
        button.innerText = "I\'m clicked"
    }
</script>
```

Learning Javascript these days is very benificial since you are not only write it for website. You can also use it in other things (now you can use your ChatGPT).

Oh yeah, using `<script>` tag is a way to use Javascript internally in your HTML. But you can also create a `.js` file and import it like this :

```html
<script src="somejsfile.js"></script>
```

### Conclusion

Congratulation, you can now add **Web Development** skill to your resume.

Well, actually not yet....

Go create a new folder and open it in your Code Editor then create your own website. I'll be posting new article about making a simple Landing Page, so stay tune.