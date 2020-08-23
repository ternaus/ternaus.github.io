---
layout: single
title:  "I trained a model. What is next?"
excerpt: "I wish I knew it when I was active at Kaggle."
categories: tutorial
tags: kaggle python machine_learning deep_learning

---

{% include toc title="Table of Contents" %}


To build machine learning muscles, I participated in machine learning (ML) competitions at Kaggle and other platforms. Every challenge ended with new knowledge, code, weights for trained models.

I loved my learnings but ignored the value that my ML pipelines could bring. Code stayed in private GitHub repositories.

I trained models for months, they lead me to the top of the leaderboard. After the end of the challenge, all of them were deleted.

The situation is not unique to competitions. People in academia train models, write a paper. After the article got accepted, they delete all model artifacts to free some space at the disk.

In this blog post, I will talk about a few small steps that you can do on top of your modeling work that will:

* Boost your technical knowledge
* Build your personal brand
* Improve your career opportunities
* Make the world a better place  :)

As an example I will use the repository [https://github.com/ternaus/retinaface](https://github.com/ternaus/retinaface)


## +5 min: Release your code to Github Public repo

Most likely, your code is already at Github, but it is not available to the public. Think about it carefully. What will you lose if you release it?

There are situations when it is not possible, but in the case of your pet project, your Kaggle solution, or your paper, it may not be the case.

The most common obstacle is that people think that their public code should be perfect, that they will be judged.

In reality, no one cares. Just do it. Release it as is, without any polishing.

Making code public is an important psychological step. Releasing non-perfect code is a confident, bold move.

Besides, all later steps are based on this.

Example: [https://github.com/ternaus/retinaface](https://github.com/ternaus/retinaface)

## +20 min: Improve readability

You can improve the readability of your python code by adding syntax formatters and checkers.

It is not hard, and it will not take a lot of time. It will not transform bad code into a good one, but it will make it easier to read. Think about fixing syntax as about basic hygiene. It is like brushing your teeth, but for the code.

I wrote a blog post on this topic called [Nine Simple Steps for Better Looking python code](http://ternaus.blog/tutorial/2020/04/09/Nine-simple-steps-for-better-looking-python-code.html). Feel free to check it out.

### Step 1: configuration files

* [setup.cfg](https://github.com/ternaus/retinaface/blob/master/setup.cfg) - configuration for flake8 and mypy
* [pyproject.toml](https://github.com/ternaus/retinaface/blob/master/pyproject.toml) - configuration for black

### Step 2: requirements

```bash
pip install black flake8 mypy
```

### Step 3: black

There are 100500 ways to format the code. Formatters like black or yapf modify the code to satisfy a pre-defined set of rules.

It is easier to read the code that has some standards. When you work on the code for hours, every time you need to switch a context from one code style to another, you lose "willpower energy"—no need to do it without a good reason.

Running
```bash
black .
```
will reformat all python files in the repo to follow the set of rules by black.

### Step 4: flake8

Running
```bash
flake8
```

will check your code for syntax issues and output them to the screen.

Fix them.

### Step 5: mypy

Python does not have mandatory static typization, but it is recommended to add types to the function arguments and return types.

For example:
```
def add_tensor(a: torch.Tensor, b: torch.Tensor) -> torch.Tensor:
    return a + b
```

I recommend adding this to your code.

1. It makes code easier to read
2. You can use a mypy package to check argument and function types for consistency.

After you added static typization to the code you can run mypy on the whole repo:

```
mypy .
```

If mypy found issues - fix them.

### Step 6: pre-commit hook

Running **flake8**, **black**, **mypy** manually all the time is annoying.

There is a tool called **pre-commit hook** that adreses the issue

To enable it - copy this file to your repo: [.pre-commit-config.yaml](https://github.com/ternaus/retinaface/blob/master/.pre-commit-config.yaml).

You will need to install the pre-commit package on your machine with:

```bash
pip install pre-commit
```

And initialize with
```bash
pre-commit install
```

You are good to go.

From now on, on every commit pre-commit will run a set of checks and not allow the commit to passing if something is wrong.

The main difference between the manual running of the black, flake8, mypy is that it does not beg you to fix issues, but forces you to do this. Hence, there is no waste of "willpower energy."

### Step 7: Github Actions

You added checks to the pre-commit hook and you run them locally. But you need a second line of defence. You need Github to run these checks on every push.

Way to do it is to add file [.github/workflows/ci.yaml](https://github.com/ternaus/retinaface/blob/master/.github/workflows/ci.yml) to the repo.

There are lines:
```yaml
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt
        pip install black flake8 mypy
    - name: Run black
      run:
        black --check .
    - name: Run flake8
      run: flake8
    - name: Run Mypy
      run: mypy retinaface
```

that tell Github what to check.

When you have this file in the repo, Github will run listed checks on every pull request.

I also recommend you to give up the practice of pushing the code directly to the master branch.

Create a new branch, modify your code there, commit, push to Github and create pull request.

It is a standard in industry, but it is extremely uncommon in the academy and among Kagglers.

If you are not familiar with these tools, it can take more than 20 minutes to add them and fix all errors and warnings that they will find.

Remember this time. In the next project, add these checks in the first commit. After this, you will only need to fix only a few lines of code every time: tiny overhead, excellent habit.

In addition I would recommend to read a book [Atomic Habits: An Easy & Proven Way to Build Good Habits & Break Bad Ones](https://amzn.to/32fIaiO). It talks about small changes in your behaviour and your processes to improve your productivity and the quality of your life.

## III: +20 min: Create a good readme.

Good readme serves two purposes:
* For yourself: you think that you will never use this code, but "never say never." You will, and you will not remember what was happening here. And readme will help you.
* For others: Readme is a selling point. If a person cannot tell the purpose of the repo and what problems it addresses, people will not use it. All the work that you did will not have a positive impact on others.

For machine learning repositories, the bare minimum is:
* An image that tells the visitor what the task was and how did you solve it. No words should be required. Most likely, you have 100500 pictures after working on your problem for weeks. They are just not a part of the readme. Fix it.
* Where to put the data.
* How to start training
* How to perform inference.

If you need to write 100500 words to describe how to run training or inference it, it is a flag. You need to refactor your code and make it more user friendly. People often ask - how can I become a better programmer? This is the exercise that helps with this. You will need to rewrite your code. Famous: "Customers first."


Example: For retinaface, I wrote a [wrapper over a model](https://github.com/ternaus/retinaface/blob/master/retinaface/predict_single.py) that hides details of the postprocessing from the user.

Note: Readme created at this stage will be reused later when we will build a library.

## IV: +20 min. Make it easy to use your trained model.

I would guess, you write

```python
model = MyFancyModel()
state_dict = torch.load(<path to weights>)
model.load_state_dict(state_dict)
```
to load pre-trained weights to the model.

It works and steps are clear, but it requires to have weights on the disk and know where they are. A more elegant solution
is to leverage the `torch.utils.model_zoo.load_url` function in torchvision and similar in tensorflow or keras.

We can do something like:
```python
from retinaface.pre_trained_models import get_model

model = get_model("resnet50_2020-07-20", max_size=2048)
```
If weights are not on the disk they are loaded from the internet and cached on the disk.
Model is initalized and weights are loaded.

This is user friendly and that is what you see in torchvision and timm libraries.

### Step 1: host weights of the pre-trained model

This was the biggest blocker for me. Where can I put weights for the model if you do not want to deal with AWS, GCP?

Apparently, there is an excellent solution, I would even say a loophole. You can put upload weights to the releases at GitHub.

IMAGE!!!! with arrow

The limit is 2Gb per file, which is enough for most Deep Learning models.
### Step 2: write a function that initializes the model and loads weights

In my case it was:

<script src="https://gist.github.com/ternaus/8c4bdc5b3695e420db76874261092c1a.js"></script>

Note: This functionality will beleveraged when we will build Colab Notebook and WebApp.

## V: +20 min. Make a library.

In this step, you lower the entry point for others to use your model. The goal is to perform predictions without `git clone retinaface`.

### Step 1: add necessary dependencies to the requirements.txt

### Step 2: change the file structure of the repo

Create a "main folder," in my case, it was called "retinaface," the same as the repository.
* Move all the important code there.
* Do not move helper images, Readme, or notebooks tests there. No need to add them to the library

Doing it manually and updating all imports would be painful. PyCharm or similar IDE will do it for you.

This is a common way to structure code in the repositories.

I hope, in the future, you will follow this pattern from the beginning. If you want something even more structured, check out [Cookie Cutter](https://github.com/cookiecutter/cookiecutter) package.

### Step 2: add config file.

You need to add setup.py to the root of the repository. Just copy paste one from retinaface and modify the necessary fields.

* Add setup.py to the root of the folder with the content similar to [setup.py](https://github.com/ternaus/retinaface/blob/master/setup.py)
* Add a version for the package. In my case, I added it to the [init file](https://github.com/ternaus/retinaface/blob/master/retinaface/__init__.py) of the "main" folder.

### Step 3: Create an account at PyPI
If you do not have an account at [PyPI](https://pypi.org/), you need to create it.

### Step 4: Build library and upload to PyPI

```bash
python setup.py sdist
python setup.py sdist upload
```

That is it. You repository is a library and everyone will be able to install it with

```
pip install <your_library_name>
```

If you check the page of your package at PyPI you will see that it uses readme that you have in the repo to present the project.

Note: We will use the functionality of this step for Google Colab and for a Web App.

VI: +20 min. Create a Google Colab notebook.

It is a good practice to add a jupyter notebook to the repository to show how to initialize the model and perform inference. [Example](https://github.com/ternaus/TernausNetV2/blob/master/Demo.ipynb).

We can do better.

In the previous two steps we enabled “fancy” model initialization and the `pip install ` magic. Let's leverage this.

We can create Google Golab notebook.

Now, the only thing that someone needs to play with your model is browser! Even more people will be able to check your model.

[Example](https://colab.research.google.com/drive/1wLXZyoybDRKizfcIzxPwkeYp-XDpTM-K?usp=sharing#scrollTo=0iI1uHI7ZoTM).

P.S. Do not forget to add a link for notebook to your readme and update version at PyPi.

VII: +20 min. Create WebApp

Many Data Scientists assume that building a web app is a complicated procedure that requires specialized knowledge.

This assumption is correct, the web app for a complex project requires skills that Data Scientists may not have.

But building a simple web app that demonstrates the model is easy.

I created a separate [github repository](https://github.com/ternaus/retinaface_demo) for a webapp, but you can do it in your repository with the model.

Blog post that describes details: [How to Deploy Streamlit on Heroku](https://towardsdatascience.com/deploy-streamlit-on-heroku-9c87798d2088)

### Step 1: Add code for the app.

[Code](https://github.com/ternaus/retinaface_demo/blob/master/app/app.py)

```python
"""Streamlit web app"""

import numpy as np
import streamlit as st
from PIL import Image
from retinaface.pre_trained_models import get_model
from retinaface.utils import vis_annotations
import torch

st.set_option("deprecation.showfileUploaderEncoding", False)


@st.cache
def cached_model():
    m = get_model("resnet50_2020-07-20", max_size=1048, device="cpu")
    m.eval()
    return m


model = cached_model()

st.title("Detect faces and key points")

uploaded_file = st.file_uploader("Choose an image...", type="jpg")

if uploaded_file is not None:
    image = np.array(Image.open(uploaded_file))
    st.image(image, caption="Before", use_column_width=True)
    st.write("")
    st.write("Detecting faces...")
    with torch.no_grad():
        annotations = model.predict_jsons(image)

    if not annotations[0]["bbox"]:
        st.write("No faces detected")
    else:
        visualized_image = vis_annotations(image, annotations)

        st.image(visualized_image, caption="After", use_column_width=True)
```

Less than 40 lines.

### Step 2: Add config files.

You will need to add files:
* [setup.sh](https://github.com/ternaus/retinaface_demo/blob/master/setup.sh) - you can use this file without changes.
* [Procfile](https://github.com/ternaus/retinaface_demo/blob/master/Procfile) - you will need to modify path to the file with app.

### Step 3: Add requirements.txt

### Step 4: Register at herokuapp

### Step 5: Push the code

```bash
heroku login
heroku create
git push heroku master
```

You are live. Check out the example for [https://retinaface.herokuapp.com/](https://retinaface.herokuapp.com/)


## VIII: +4 hours. Write a blog post.

Many people undervalue their work. They assume that if they know how to do something, everyone knows it. It is not the case.

>One man's trash is another man's treasure.

Your article will help other people and improve your career opportunities.

I work at Lyft, Level5, and apply Deep Learning techniques to self-driving problems. Before Lyft, I worked at the debt collection agency TrueAccord. You can read about my job search in the blog post: "Shifting Careers to Autonomous Vehicles."

One of the reasons I was able to do this career shift is because I shared my knowledge in blog posts and meetups.

Worked for me - will work for you.

For machine learning, I would recommend writing the text that covers:

What was the problem?
How did you solve it?

If you read till this moment and found this article useful, you can say "Thank you!" by writing a blog post about one of the machine learning problems that you faced and how you solved it.

Example:
* Challenge: [IEEE's Signal Processing Society - Camera Model Identification](https://www.kaggle.com/c/sp-society-camera-model-identification)
* Blog post: [Forensic Deep Learning: Kaggle Camera Model Identification Challenge](http://ternaus.blog/machine_learning/2018/12/05/Forensic-Deep-Learning-Kaggle-Camera-Model-Identification-Challenge.html)


### IX: Days. Write a paper that describes your solution to the machine learning competition.

Even if your paper is not a breakthrough, it will be published and have value to other people.
Writing papers is a separate skil and you may not have it now. Not a problem. You can collaborate with people that
know how to write in academic format.

Examples:
* [Deep Convolutional Neural Networks for Breast Cancer Histology Image Analysis](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3Dvkjh9X0AAAAJ%26citation_for_view%3Dvkjh9X0AAAAJ%3ATQgYirikUcIC%26tzom%3D420) 100 citations.
* [Automatic instrument segmentation in robot-assisted surgery using deep learning](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3Dvkjh9X0AAAAJ%26citation_for_view%3Dvkjh9X0AAAAJ%3AR3hNpaxXUhUC%26tzom%3D420) 100 citations.
* [Paediatric bone age assessment using deep convolutional neural networks](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3Dvkjh9X0AAAAJ%26citation_for_view%3Dvkjh9X0AAAAJ%3AmB3voiENLucC%26tzom%3D420) 70 citations.
* [Ternausnet: U-net with vgg11 encoder pre-trained on imagenet for image segmentation](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3Dvkjh9X0AAAAJ%26citation_for_view%3Dvkjh9X0AAAAJ%3AHDshCWvjkbEC%26tzom%3D420). My favorite example. The idea was trivial. This work was written for fun as an addition for the code at GitHub. We did a mistake and did not submit it to the conference. We assumed that noone would be interested. It is my most cited work.

Just look at my [Google Scholar](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en#). Bump in the previous few years comes from the papers that were summarizing participation in different machine learning competitions.

![](https://habrastorage.org/webt/nj/uj/wi/njujwinbk9kwjeltf1ry8yll2vc.png)


Besides - your paper will not be alone. It comes in a package with:

* Github repository that has clean code and a good readme.
* A library that non-machine learning people can use.
* Colab notebook that allows fast experiments with your model in the browser.
* WebApp that engages the non-technical audience.
* The blog post that uses human being language to tell the story.

It is not a paper anymore, it is a cohesive strategy that shows your "ownership" and "communication." Both are crucial for your career growth, but I will talk about it next time :)
