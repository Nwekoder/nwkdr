---
title: REST API as Fast as Possible
published: 2024-11-14
description: 'Trying out FastAPI to create a simple REST API with Python.'
image: ''
tags: ['Python', 'FastAPI', 'Back End Development']
category: 'Tech Showcases'
draft: false 
lang: 'en'
---

## What is FastAPI

According to it's [official website](https://fastapi.tiangolo.com/),
<blockquote>
FastAPI is a modern, fast (high-performance), web framework for building APIs with Python based on standard Python type hints.
</blockquote>

In other word, it's a "web framework" that are easy to learn (what you expect from Python) for building APIs that are both fast to develop and high performance. Which means it's very good start for those who want try to learn Back End Development without too much efforts and headache.

## Difference between Flask and FastAPI

Well.... FastAPI is much newer to ears than Flask, which means it would adopt what newer Python version has to offer. Personally, I didn't even know that Python has "type annotations" until I update to the latest Python version (around version 3.12.x).

## Experiment Begins

### - What will you need

- Python (I'm using version 3.13.0, ftb)
- Code Editor (VS Code with Essential Python Extensions is Recommended)
- Cup of Coffee (or Tea)
- Some Snacks (or Cigarettes if you like me)

### - Installing FastAPI

I'm on Windows 11, so just open your terminal and use this command

```cmd
pip install fastapi[all]
```

This will download all FastAPI modules and including the fastapi CLI to run our app later.

### - Your first REST API Endpoint

Just make a new directory and open that directory on your Code Editor. Next, just create a new Python file and then import some stuff from `fastapi`.

```py
from fastapi import FastAPI
```

That will import the FastAPI class that we can use to initiate a new FastAPI Instance. Next, just create a variable that initiate the class that we import earlier.

```py
app = FastAPI()
```

Now for our first endpoint. You can create a GET endpoint just by doing this.

```py
@app.get('/hello')
def get_hello():
    return {
        "message": "Sup"
    }
```

In my opinion, this "hello world" code is much cleaner than what I used to made using Express.js in Javascript world.

### - Run your FastAPI App

To run this app, we're going to use FastAPI CLI that were included. Just run this command and the app should be running at port 8000.

```cmd
fastapi dev <your-python-file>
```

## Conclusion

FastAPI is great for almost any type of projects especially if you already familiar with Python and other modules for ORM, Tokenization (JWT Stuff) and many more. It's simple and clean way to create APIs are fantastic, the documentations are also very easy to understand even for beginners. There's so much to cover about FastAPI, but it might be best if you just check out it's [official website](https://fastapi.tiangolo.com/).