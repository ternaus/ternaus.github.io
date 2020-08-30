---
layout: single
title:  "Cross-post of the interview at toolbox.com"
categories: interview
tags: interview career self_driving

header:
    teaser: https://images.toolbox.demandshore.com/33/b6/acab4acf430dae7ff6e842e365e0/vladimir-iglovikov.png
    og_image: https://images.toolbox.demandshore.com/33/b6/acab4acf430dae7ff6e842e365e0/vladimir-iglovikov.png
---
![](https://images.toolbox.demandshore.com/33/b6/acab4acf430dae7ff6e842e365e0/vladimir-iglovikov.png)

The interview qas originally published at toolbox.com: [Lyft Computer Vision Expert on Why Ridesharing Is the Future of Mobility](https://www.toolbox.com/tech/big-data/articles/lyft-on-why-ridesharing-is-the-future-of-mobility/).

{% include toc title="Table of Contents" %}

---
>Self-driving companies are not the only ones that are preparing for the future with autonomous. Government officials and people that work on city planning are seriously discussing how to accelerate the effort.

The coronavirus crisis has spotlighted the usefulness of autonomous technology, with self-driving cars chipping in for [COVID-19](https://www.toolbox.com/tech/tech-security/blogs/amid-covid-19-attacks-on-financial-and-food-beverage-industries-peak-reports-imperva-041720/).
Government [authorities](https://www.jtafla.com/media-center/press-releases/jta-beep-navya-autonomous-shuttles-help-mayo-clinic-transport-covid-19-tests/) in the U.S. are rising to the challenge by deploying autonomous shuttles to transport medical supplies and COVID-19 tests. The pandemic has also brought to the fore several new use cases for AVs that are put into action for shuttling essential goods to limit the spread of contagion and deliver a contactless experience. Post -pandemic, there will be a push for widespread adoption of autonomous vehicles (AV) that will become a viable and trusted travel option in the future.

In an interview with Toolbox, [Vladimir Iglovikov](https://www.linkedin.com/in/iglovikov/), Senior Computer Vision Engineer at Level 5, Lyft’s Self-Driving Division discusses the work underway to productionize self-driving cars, and how ridesharing (Level 4 autonomy) will be the way that most people experience the best of the autonomous tech in the future. Along the way, the Kaggle Grandmaster also reveals how future cities will be built for [autonomous vehicles](https://www.toolbox.com/tech/devops/blogs/uber-co-founder-travis-kalanick-quits-the-board-sets-sight-on-new-venture-cloudkitchens-122719/). In addition, Iglovikov, the co-creator of an open-source library [albumentations](https://albumentations.ai/) dishes out best practices on how Kaggle can help data science enthusiasts build machine learning skills and how modern-day ML has hugely benefited from open-source libraries at nearly every step.

#### Key takeaways from this interview:

* How machine learning competitions on Kaggle are a good starting point for ML enthusiasts
* Key skills to invest in to begin a career in autonomous driving technology
* Existing roadblocks in the industry to scale end-to-end self-driving experience

Here’s the edited transcript of the interview with **Vladimir Iglovikov**:

## Can you walk us through your journey from majoring in theoretical high-energy Physics to becoming a Kaggle Grandmaster, becoming an expert in Machine Learning, Deep Learning, and Computer Vision, and finally joining the Level 5 team at Lyft?

In 2015, I was finishing my doctorate degree in theoretical physics at UC Davis. I did not want to stay in academia and was debating if I should become a software engineer. My friend, who moved to Silicon Valley got me excited about data science, so I decided to apply for data science positions.

I finished my thesis and also took online courses in data science prior to graduating. In one of the courses, the lector mentioned the Kaggle platform as an excellent place to practice machine learning skills (ML), so I checked it out and joined Kaggle immediately. Kaggle is a platform that hosts machine learning competitions and is a great place to practice ML skills, as well as the ability to learn from other people.

I actively participated for a few years. Initially working on problems in traditional machine learning, but when deep learning and computer vision became more popular, I shifted my focus to this domain. Kaggle tries to engage the community using gamification techniques. In particular, it has titles like [Expert](https://www.kaggle.com/progression#expert), [Master](https://www.kaggle.com/progression#master), and [Grandmaster](https://www.kaggle.com/progression#grandmaster) that are awarded for the achievements on the platform. There are about 3,000,000 people registered on Kaggle. Only 200 of them are Grandmasters. It took me a while to get to this level, but during the process, I was competing with the best of the best while also learning from them. It was useful for my career to merge my academic background, along with participating in Kaggle, and having industry knowledge to earn my position at Lyft’s Level 5.

Prior to Lyft, I worked in a company called TrueAccord. The path to getting to Lyft was challenging, and I highlighted this via a [blog post](https://ternaus.blog/career/2020/01/08/How-I-Found-my-current-job.html) I wrote about the journey. It’s helpful for people who are thinking about getting into a different career, such as debt collection to self-driving cars — feel free to check it out.

## Over the past few years, we have seen many data scientists transition from Physics to Machine Learning and Artificial Intelligence. Can you draw parallels on how Physics lends itself to AI?

I believe Physics and [Machine Learning](https://it.toolbox.com/tech-101/data-science-vs-machine-learning-top-differences) are really well aligned.

First, the level of Math that you learn in Physics is a few decades away from what you use in modern Machine Learning. This makes the theory behind machine learning easy to understand.

Second, and the most important is the mindset. In Physics, people are maneuvering between rigorous theory and actual data, trying to connect them sensibly. Machine Learning is very similar.

I may be biased about the alignment of Physics and machine learning. Still, I know at least 20 Kaggle Grandmasters that have Physics majors.

## Did participating in data science challenges through Kaggle help you learn more about ML and DL? In your opinion, does Kaggle, with its pre-cleaned datasets, help in polishing coding skills?

I never took any Machine Learning classes in universities. It is hard for me to judge how good the courses are at universities. The only exception is the [CS231n, the introduction to convolutional neural networks](http://cs231n.stanford.edu/) that I watched on YouTube, and that course was excellent.

I believe that competitions and classes complement each other.

In theory, working on machine learning competitions looks like this: you study everything, you come to the competition, you win it. Yeah, sure, the reality is different. Typically you come to the competition, and you instantly realize that your understanding of the problem is minimal, and you need to learn many new things.

When the participant works on a challenge, he or she is actively reading scientific literature, watching online courses, or finding any other way to study.

Regarding the data, I would not say that it is clean. There is a decent amount of effort that goes into building preprocessing pipelines that clean the data up and help fix incorrect labels. If someone said that Kaggle does not teach you data cleaning or feature engineering, I would disagree.

But what I will agree with is that competitions do not help with polishing your coding skills. When you write code at work, you need to write it well. It should be modular, well tested, well designed, well documented. Most likely, your code will stay in production long after you leave for another job. Competitions are different because you want to win and get to the top. Everything else is important, but secondary. Besides, after the competition is over, you will most likely scratch your code. You will not learn how to write production quality code in competitions.

## What are the go-to tools of data scientists in the self-driving research field? What are the tools/algorithms you use frequently for autonomous driving? For a learner interested in autonomous driving, what kind of path would you recommend?
If we are talking about machine learning:

* Deep Learning frameworks: Tensorflow / Pytorch.
* Programming languages: Python, C++.
* Algorithms: Depends on the task. For the perception of imagery and Lidar data, convolution neural networks. For prediction and planning some other algorithms. Not sure how much I am allowed to tell here

If you are interested in getting a job in autonomous driving, I would recommend investing in software engineering skills.

A strong software engineer with basic knowledge in machine learning has higher chances to get a job compared to a person who is good at machine learning but has a basic engineering skillset. Autonomous tech is very complex. To build it, to improve it, you will need to write a lot of high-quality code. I would recommend focusing on this. And if you want to practice your ML muscles, just do Kaggle and try to get to the Kaggle Master level.

## Can you throw light on how open source tools like PyTorch, availability of training and validation data, and pre-trained models help beginners experiment with this exciting domain? Lyft has open-sourced its tools and libraries. How do these steps empower the developer community?

Proper tools, useful data, and good pre-trained models are crucial components in any machine learning domain. It is hard for me to imagine modern-day machine learning without the use of open-source libraries at nearly every step.

I can speak about [open sourcing](https://www.toolbox.com/tech/data-center/interviews/scality-ceo-on-why-the-future-of-infrastructure-is-open-source/) from my perspective. In my free time, I work on an open-source library for image augmentations [albumentations.ai](https://albumentations.ai/). At some point, my collaborators and I decided to release the code that we were copying from one winning Kaggle solution to the other as an open-source product.

In the last year, the library is used in almost all winning solutions at Kaggle. It is used in academia, and some companies, including Lyft, use it for model development.

I believe that contributing to open source is a good way to contribute to the community. We develop a lot of excellent tools at Lyft. I hope that we will continue open-sourcing what we developed internally.

About the data. One of the reasons autonomous vehicles aren’t more common on roads is that more research is required. The problem is that the research community does not have access to the useful datasets that are relevant to the problem.
Last year Lyft and other companies released labeled datasets that combine Lidar and images data and that are used for developing perception systems in autonomous technology. In addition to this, we collaborated with Kaggle and hosted the competition on this dataset.
I loved this initiative and [helped with the organization](https://www.kaggle.com/c/3d-object-detection-for-autonomous-vehicles/discussion/133895). We hope this helped the community.

## To add to the above question, how has OpenDataScience as a community, of which you are an active member, helped young developers hone their skills and learn more about AI/ML job requirements?

Open Data Science ([ODS.AI](https://ods.ai/)) is a Russian speaking [data science](https://it.toolbox.com/tech-101/data-science-vs-machine-learning-top-differences) community. Currently, 42,000 people are registered. This is a large, diverse field of people from all over the world, varying from high school students to professionals from the industry to academia and industrial research labs as DeepMind and OpenAI. All top Russian speaking Kagglers are also there.

There are a lot of conversations happening regarding data science, machine learning, business ideas, and career support. One of the advantages of the community is the low tolerance to inefficiencies, which drastically improves the level of communication.

I hope that my discussions in the community helped other people, but what I know for sure is that the members of the community helped me a lot.

## What are the current roadblocks to the widespread adoption of self-driving vehicles across the globe? Industry insiders believe driverless cars will arrive by 2035.

The problem of self-driving vehicles is hard. Many things are new and unclear. I believe that the biggest roadblock is technology. The field of machine learning is advancing fast, but the tasks that we are facing are not easy at all. Changes that we have seen in the past 15 years are enormous. If we advance at a similar pace, everything could be possible.

There is another option. Self-driving companies are not the only ones that are preparing for the future with autonomous. Government officials and people that work on city planning are seriously discussing how to accelerate the effort. I have heard about the initiatives to add special lines for self-driving or even to [build cities](https://asia.nikkei.com/Economy/China-intends-for-self-driving-cars-to-propel-smart-megacity) designed for autonomous vehicles. I believe that if it was implemented, this could help to speed things up.

## Can you tell us about your learnings from the Robotaxi pilot program that involves Lyft’s partnership with Aptiv? Do we need more partnerships in the autonomous driving sector to hasten innovations in the field?

I don’t work very closely on that program with Aptiv. I know that Aptiv works with Lyft’s [open platform](https://self-driving.lyft.com/partners/) initiative, and I think this is a great idea. When the self-driving industry reaches level 4 autonomy, ridesharing will be the way that most people experience this technology. Ridesharing is hard and self-driving is hard — the open platform initiative allows both sides to get familiar with the setup.

## Lyft open-sourced its self-driving technology research work last year, letting developers and the academia access 3D frames, high-res maps and other data gathered from cameras, radar and sensors. Six months on, has the initiative helped the Level 5 team benefit from new ideas and suggestions from the industry and academia?

When we scoped last year’s competition, our goal was to promote the dataset within the community and to get people used to it.

As a result, the participants could:

1. Use any hardware for training and for inference.
2. Use any external data for training.
3. No limitations on the model size and inference time.

It worked. People struggled a lot, trying to get used to many different coordinate systems and ways to look at the data. But finally, helper functions and visualization tools were developed.

In the car, the situation is different. We have all types of limitations, but we also have the information from other sources. Hence not all ideas that were used in the challenge could be easily transferred to the car. But some ideas that the participants developed were pretty impressive.

The idea of sharing and increasing transparency could also be extended from datasets to other things.

I would love to see something like OpenStreetMaps but for HD Maps. All self-driving companies in Silicon Valley generate maps of the same region independently. It would be expensive, hard work. It would be nice to remove the duplication and improve the coverage. [Britain is already looking into this](https://www.geospatialworld.net/blogs/britain-forefront-hd-mapping-standardization/).

More on the competitions. I have seen how machine learning competitions helped to advance the field. I have read how DARPA Challenges started and advanced self-driving tech. I firmly believe that we need a regular challenge where different autonomous companies have the same environment to show how good they are. Of course, it is just a proxy of the real world. But at least we would be able to avoid the situation that we have now when we compare companies testing in Phoenix vs. others in China. It is like asking who is stronger? Elephants or whales? If any government officials will read this part, try to think about it. I would be happy to help to set such a competition up.

## In your opinion, what are the emerging trends in the autonomous vehicles industry for 2020 and beyond?

One trend is that companies will try to optimize for excellent performance in some regions and look for ways to productionize the technology rather than to solve the general problem.

## Technology research is hard work and the chances of burnout among researchers are high. What advice would you give to young data scientists and engineers to stay motivated while racing against deadlines?

The main idea is that typically very important deadlines that people face at work on the scale of the universe and even on the scale of their lives do not mean that much. I am not saying that you should not care about deadlines, but you need to estimate what the price of the mistake is. Do you really believe that this project is more important than the smile of your kid or your significant other?

When you are burned out, it is not just your problem; it is a problem of all the people around you, people that care about you. You need to be efficient, you need to be focused. But this does not mean spending 100% of your time and energy on the project.

What tips would you recommend for time management?

A good book on the topic [Deepwork](https://amzn.to/34O8h38).

1. I check emails once a day. I believe that the habit of checking what is new in your mailbox, LinkedIn messaging, Facebook, Twitter, Instagram, etc. more often than once a day is terrible. Extremely time-consuming. If your job does not allow you to check emails one a day, check them in batches, a few times a day but in 15-minute chunks. Fewer times you switch contexts, less [ego depletion](https://en.wikipedia.org/wiki/Ego_depletion) you will encounter.
2. Morning is the most productive time. Try to spend the first 4 hours of the day on the projects that require your full attention and have meetings in the afternoon.
3. If possible, do not focus on your projects after 6 pm. You may even consider to do digital detoxification and not to use your computer during that time. It will help you to recharge and, in addition to your good sleeping habits will increase your memory and cognitive abilities.
4. Have a to-do list in which you add what you need to do.
   * If an activity could be done in a couple minutes, say, send an email, do it instantly, without delaying and adding to the list.
   * It is better to have one joined list for work and personal stuff. Handling two lists is challenging.
   * When you are revisiting your to-do list, think what action items could be removed entirely. I like an example of how Steve Jobs made Apple great again. When he came back to Apple, he asked all teams to present their projects. He was lost by the number of different things that the company was working on. He cut almost all of them, leaving only four that were the most important. I recommend the book on the topic [Steve Jobs by Walter Isaacson](https://amzn.to/2YORIjN). I do something similar. If there is an important entry in my list that is there for a long time, it is probably not important at all.

5. Minimize meetings at work. Some people are proud of how full their calendar is. To build something, to invest in learning new things you need to have big chunks of the free time. In general you need to optimize for the bottleneck. Typically it is time, energy or lack of information. Focus on one that is the largest issue. For example, when you join a new company or a new team, your bottleneck is the lack of information; hence you need to attend many meetings to get the full picture. At the same time, when you are in the execution mode, most of the meetings fail in the category “nice to have.” They should be avoided.
   * A good book on the topic: Mom’s test. It helps to communicate with the partner teams and decrease the number of different follow-ups that many meetings have.
   * Another good book, which is slightly outdated, but still worth reading is The 4-Hour Workweek.
   * When you organize your meetings, try to prepare for them. For sure, it will take an extra 15 minutes of your time, but it will save many hours of the time for other people.

Try to find a support group or mentor. Many things could be significantly speeded up if you have someone to ask. Say, I use the expertise of ODS.AI when I am facing problems with machine learning. I can read all the relevant papers, but there are faster ways.

Investing in better software engineering skills is a good idea. Senior Software engineers are at least 10 times more productive than junior engineers. It takes time, but earlier, you will start – better. The best way to do it is to be a part of the team with high coding standards. If you are still in academia, you may contribute to open-source software. Feedback from the maintainers on your pull requests will teach you a lot.

## In closing, what books would you recommend to peers and colleagues on AI and ML applications in self-driving tech? And what’s on your reading list for 2020?

When I joined Level 5, I had minimal understanding of how everything works and how we got to where we are currently.. The book that gave me a good historical overview is called [Autonomy: The Quest to Build the Driverless Car — And How It Will Reshape Our World](https://amzn.to/2YNYAOo). If you are thinking about going into self-driving, I would recommend starting with it. I do not know what will be my full reading list for 2020, but while writing today, I realized that it is the time to finish [On Writing Well: The Classic Guide to Writing Nonfiction](https://amzn.to/2ENLjhA).

**About Vladimir Iglovikov**: [Vladimir Iglovikov](https://www.linkedin.com/in/iglovikov) is Software Engineer at Lyft’s Level 5 working on the mapping team. He’s also a mountaineering, rock climbing, Burning Man-loving scientist who holds both a Master’s and Ph.D. in Physics. He has published a number of [papers](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en) on everything from theoretical physics to the application of deep learning on forensics, medical, and satellite imagery and is a Kaggle Grandmaster.

**About Lyft**: [Lyft](https://www.lyft.com/) was founded in 2012 and provides millions of rides daily as one of the largest and fastest-growing transportation networks in the United States and Canada. As the world shifts away from car ownership to transportation-as-a-service, Lyft is at the forefront of this massive societal change. Our transportation network brings together rideshare, bikes, scooters, car rentals and transit all in one app. We are singularly driven by our mission: to improve people’s lives with the world’s best transportation.

**About Behind The Scenes**: [Behind the Scenes](https://it.toolbox.com/behind-the-scenes/postman-kin-lane) is a Toolbox interview series with technology evangelists and developer advocates working in the big data, cloud, AI/ML, data science and machine learning domain. The conversation is geared at inspiring developers and enthusiasts to know more about the field and gain an understanding about starting a career in that field.
