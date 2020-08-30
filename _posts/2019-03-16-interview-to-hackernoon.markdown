---
layout: single
title:  "Cross-post of the interview at hackernoon to Sanyam Bhutani."
categories: interview
tags: kaggle interview career

header:
    teaser: https://hackernoon.com/hn-images/0*nYLuLf4gpmhgyMuI
    og_image: https://hackernoon.com/hn-images/0*nYLuLf4gpmhgyMuI
---
![](https://hackernoon.com/hn-images/0*nYLuLf4gpmhgyMuI)
The interview qas originally published at hackernoon: [Interview with Kaggle Grandmaster, Senior CV Engineer at Lyft: Dr. Vladimir I. Iglovikov](https://hackernoon.com/interview-with-kaggle-grandmaster-senior-cv-engineer-at-lyft-dr-vladimir-i-iglovikov-9938e1fc7c).

{% include toc title="Table of Contents" %}

---
# Part 24 of The series where I interview my heroes.

Today, I’m honored to be talking to another great kaggler from the [ODS community](https://ods.ai/): (kaggle: [iglovikov](https://www.kaggle.com/iglovikov) Competitions Grandmaster (Ranked #97), Discussions Expert (Ranked #30): Dr. Vladimir I. Iglovikov

Vladimir is currently working as the Senior Computer Vision Engineer at Level5, Self-Driving Division, Lyft Inc.

Prior to Lyft, Vladimir was working as a Senior Data Scientist at TrueAccord. He has a background in Physics and holds a Ph.D. in Physics from UC Davis.

About the Series:

I have very recently started making some progress with my [Self-Taught Machine Learning Journey](https://hackernoon.com/launching-my-company-a-scholarship-and-a-webinar-277e3b66e351). But to be honest, it wouldn’t be possible at all without the amazing community online and the great people that have helped me.

In this Series of Blog Posts, I talk with people that have really inspired me and whom I look up to as my role-models.

The motivation behind doing this is that you might see some patterns and hopefully, you’d be able to learn from the amazing people that I have had the chance to learn from.

Sanyam Bhutani:​ Hello Grandmaster, Thank you for taking the time to do this.

Vladimir I. Iglovikov: Thank you for your questions. It is a pleasure. I will try to be as detailed as possible even if fewer readers are able to survive until the end. :)

If I had read a similar text four years ago at the beginning of my Data Science career, I believe my life would have been a bit easier. So it will be well worth all the writing if it will help even just one person.

**Sanyam**: You’ve done your Ph.D. and hold a Masters in Physics. How did Machine Learning come into the picture? Could you tell the readers about your Machine Learning journey?

**Vladimir I. Iglovikov**: About four years ago I was finishing my Ph.D. program at UC Davis. There were a few months left before graduation. It was time to think about my next steps. All my graduating colleagues were either going for:

Postdoctoral positions. OR
* Software Engineer positions.
* Postdoc positions were not appealing. They offer more compensation, but the jobs are similar to graduate students, including limited or no teaching responsibilities. I prefer to maximize the amount of knowledge gained per unit of time. In practice, this also means I am maximizing the number of new mistakes that I make each day. From that angle, doing almost exactly the same as I was doing for many years did not look attractive.

Moreover, the number of postdoc positions is limited and the number of applicants is high. It is unlikely that you will be accepted to your top choice job.

Software Engineering positions interested me even less. In University I was doing Theoretical Physics. Every day at work I was surrounded by discussions about subatomic particles, cosmological effects, space and time that blend together, nanofabrication and other exciting almost science fiction topics. This environment made me think that we live in the future and made my heart beat faster. The research that I was doing for many years was related to room temperature superconductivity. When/if it will come to our lives, I am pretty sure it will transform humanity as we know it. All of this looked cool and very exciting.

Software Engineers that I talked to were working on some complex projects that I did not care about. The discussions about backend, frontend, and other ends did not make the strings of my soul sing. The thoughts of spending the next few years in that field made me very depressed.

I had a few months before graduation and I needed to choose one of the directions, although none of them looked good.

Luckily, one of my friends, who graduated from our department a year before, stopped by UC Davis. We had a few beers and he told me about his occupation at the time. He was employed as a Data Scientist in a small startup in San Francisco. What he did sounded interesting. He also mentioned his compensation. And this number was a few times more than I was making as a graduate student. Money is not my driving force, but lack of money prevented me from many activities that I wanted to pursue in my life. Thus the financial component of this opportunity was hard to ignore.

I came home and decided that Data Science was worth a shot. The issue was that I had no clue what the Data Science was, what problems does it solve, and more importantly, how to land a job. The internet did not help. Time was passing. I decided to take an online class about Data Science, and I think it was a nano degree from John Hopkins.

In one of the classes, the authors mentioned Kaggle. I needed to practice what I was learning about ML. Kaggle looked like a good playground. I went through the [tutorial about Titanic mortality forecasting](https://www.kaggle.com/c/titanic#tutorials) and continued to expand my skills on new competitions.

I read blogs, books, papers, took online classes, and was searching for any other material that could expand my ML knowledge. My standing on the leaderboard in the first few competitions was low, but slowly and consistently the results started to improve. Every time I was finishing closer to the top my ML intuition was developing, and the number of strong pipelines in my private GitHub repo was growing. There were plenty of gaps in my background, but after a few months into Kaggle, I was able to look at most ML problems and give a well-educated guess on what feature engineering can work and how different algorithms would behave.

At the same time, I was trying to find a job, and it was not easy. I did not have industry experience, I did not know how to write a resume, I did not have any non-Physics networking.

I wrote the best resume I could and applied to every position that was Data Science related. I was sending them through the company websites, and we all know that the applications mostly go into a black hole.

The biggest problem was probably not the lack of technical skills, although the list of things that I needed to learn was really long, but my mindset. After so many years in academia, unconsciously, you assume that all people in the world think the same as your University colleagues. This is very far from the truth. I was able to get a few interviews, but failed miserably, some due to the limitations of my technical knowledge but some on the “cultural fit.” Interviewers felt like aliens, and they probably felt the same about me.

At the end of August 2015, I moved to Oakland. My friend has a house there and he agreed to host me for a couple of months while I was looking for a job. My credit cards were almost depleted. My visa was about to expire. If I could not get an offer in two months I would be deported. his situation motivated me a lot. In a month of job searches and aggressive studying of use-cases, Computer Science fundamentals, statistics, SQL, and other non-ML things, I was able to get an offer for a company named [Bidgely](https://www.bidgely.com/), located in Sunnyvale.

Bidgely works in the field of the internet of things, developing the technology called Energy Disaggregation. Both the product and underlying technology looked interesting.

I did not like the location. When I came to Sunnyvale I expected non stop motion, dynamics, self-flying something in the skies, meetups, conferences, people talking about their ideas for startups. I wanted to see dreamers; those that were willing to take a risk and fail if necessary. Basically, I wanted to see an image that was formed in my head about Silicon Valley from TV shows and the internet. The reality was different. Sunnyvale looks like a town after a zombie apocalypse. Empty streets, empty restaurants, empty everything. Another issue during that period was that Bidgely used MatLab as their main Data Science tool and it was a huge turn-off.

I was building knowledge at work, but it was not enough. During the day I was doing what was required for my job. In the evenings I was busy on Kaggle competitions and supplementing my knowledge with all the sources I was able to find.

I learned a lot from the team and am really thankful for the time that I spent there. But eight months later, I had the opportunity to combine all the knowledge I had acquired and start a Data Science job at a startup called [TrueAccord](https://www.trueaccord.com/). At that position, I used Machine Learning to build recommender systems, and it was not MatLab, it was god blessed python. The office was located in San Francisco which was a huge step up. There are plenty of things that I may not like in San Francisco, but the startup drive is here. Not in the form that I observed on TV shows, but still.

This combination of knowledge flow from my job and from competitions was really nice. Machine Learning that you do at your day job will not make you good in competitions and competitions will not make you good at your industry job. They address different issues, which makes their combination really powerful.

In winter 2017 Kaggle started hosting a lot of Computer Vision tasks. Computer Vision is exciting. It matched with the skill that I wanted to master.

Another issue that I had was that my learning process was not efficient. I did not have a mentor who could guide me in Machine Learning journey. My colleagues did not know and did not want to learn ML. And I did not have friends that I would be able to ask hard ML questions that were bothering me or just discuss the latest papers.

I was progressing rapidly, but struggling on the problems by my own did not feel as effective as I would like my learning to be.

Then a miracle happened. I was invited to become a member of the meritocratic Russian speaking Open Data Science community ods.ai. Finally, I had access to the community of ML experts from industry, academia, and Kaggle community. This was the next level of my ML journey. There, I met people that became my teammates in competitions, in writing scientific papers, and in the open source projects.

In the upcoming months, I got top places at:

* [3rd place: Kaggle: Dstl Satellite Imagery Feature Detection](https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection)
* [2nd place: Safe passage: Detecting and classifying vehicles in aerial imagery](https://www.datasciencechallenge.org/challenges/1/safe-passage)
* [7th place: Kaggle: Planet: Understanding the Amazon from Space](https://www.kaggle.com/c/planet-understanding-the-amazon-from-space)
* [1st place: MICCAI 2017: Gastrointestinal Image ANAlysis (GIANA)](http://endovissub2017-giana.grand-challenge.org/)
* [1st place: MICCAI 2017: Robotic Instrument Segmentation](https://endovissub2017-roboticinstrumentsegmentation.grand-challenge.org/)
**Sanyam Bhutani**: What made you pickup kaggle and continue competing to eventually become a Grandmaster?

**Vladimir I. Iglovikov**: Becoming a [Kaggle Master](https://www.kaggle.com/progression#master) is not that hard. My firm belief is that every decent ML Engineer / Researcher can and should be able to get one gold and two silver models in the Kaggle competitions. And we have plenty of examples of this being the case. It will take some evenings and weekends, but if you have a solid background in Machine Learning from self-education, academic or industrial experience, it should not be that challenging.

[GrandMaster](https://www.kaggle.com/progression#grandmaster) is a different story. There are over two million people registered at Kaggle, but only 150 of them are GrandMasters. Kaggle is a second unpaid full-time job. You need a really good reason to burn your free time for months or even years on this. There are other, much more important activities in life like traveling, sports, social life, etc. Probably, my main reason for getting to the GrandMaster level that I enjoyed working on all the problems and I was able to do it well :)

Right now I have many exciting, and challenging problems that can be addressed with Deep Learning at work. This makes me less excited about competitions, although I do a few submissions from time to time at Kaggle.

At the same time, life is not limited to work, and in addition to traveling, sports, and social activities in my free time, I am working on open-source projects.

Here I would like to mention an image augmentation library [Albumentations](https://albumentations.ai/) that Kaggle Masters [Alexander Buslaev])(https://www.linkedin.com/in/al-buslaev/), [Alex Parinov](https://www.linkedin.com/in/alex-parinov/), [Eugene Khvedchenya](https://www.linkedin.com/in/cvtalks/), and I are developing in our free time.

![](https://hackernoon.com/hn-images/0*voF4l2SQi2jbEOGV)
![](https://hackernoon.com/hn-images/0*abaQA4V1Z87IMS7E)

Another activity that takes the time that I could dedicate to Kaggle competitions is writing pre-prints, papers, and blog posts. About a year ago, just for fun, [Alexey Shvets](https://www.linkedin.com/in/shvetsiya/) and I published a pre-print called:

“[TernausNet: U-Net with VGG11 Encoder Pre-trained on ImageNet for Image Segmentation](https://arxiv.org/abs/1801.05746)”. There was nothing extraordinary in that work, just UNet + VGG11 encoder that I used in our winning solution to the [Carvana Challenge](https://medium.com/kaggle-blog/carvana-image-masking-challenge-1st-place-winners-interview-78fcc5c887a8).
The model is just some other variation of UNet, and I would not even say that it is the most successful variation.
Right now, only one year later, a pre-trained encoder is already a standard, and people use much more exciting variations with hypercolumn, squeeze and excitation modules, and other nice tricks.

As I have said, we did it mostly for fun, but when I look at my [Google Scholar profile](https://scholar.google.com/citations?user=vkjh9X0AAAAJ&hl=en), it is my most cited work.
It outperforms things that I was doing in academia for many years. When I was presenting posters for other work at CVPR 2018, people came to me and thanked me for TernausNet, for sharing the [code](https://github.com/ternaus/TernausNet), and told me how it helped them.
I knew that the enormous amount of knowledge rot at Kaggle forums without having a chance to get to the outside world and being helpful to the ML practitioners. This story with TernausNet made me feel the scale of the problem better.

Last year my collaborators and I invested a lot of time publishing papers based on competitions. It helped to share our knowledge.

The feedback from the community was positive, we got some citations for our publications, and I am planning to increase my writing activity this year even more.

![](https://hackernoon.com/hn-images/0*sUFUQVbMdBT1zpUc)

I really hope that more and more Kagglers will invest in writing. It can be blog posts, papers, or something else. More information flowing between people is better. Writing a blog post or tech report will help you to structure thoughts on the problems, it will help other people to have a warm start on similar challenges and, most likely, it will help you with career opportunities. Which means that you will work on more exciting problems and being better paid at the same time.

**Sanyam Bhutani**: Today, you’re working as a Computer Vision Engineer at Lyft.
Do you feel the kaggle competitions are related to your work? How do you find the time to kaggle?

**Vladimir I. Iglovikov**: When I was interviewing for Lyft, I wanted a position that involved the application of Deep Learning to Computer Vision tasks. My major in university was Theoretical Physics which, in my biased opinion, is superior to Computer Science. But the representatives of the Human Resources (HRs) department had an opposite view. I did not have any Computer Vision related publications in my resume and my work before Lyft was about traditional Machine Learning and not imagery data. The only thing that was related to what I wanted to do were the top results in the Computer Vision competitions.

Typically, HR skips parts of your resume about the results in competitive machine learning and look for a set of standard resume filtering keywords. This time a miracle happened and Kaggle results attracted attention. It helped me to get into the interviewing pipeline. Now having experience developing and deploying Machine Learning models in my previous companies in combination with the knowledge obtained at Kaggle, interviews were relatively straightforward. Hence, Kaggle experience and achievements helped me to get a job that aligned with what I wanted to do.

At the same time, it is non-obvious that Kaggle competitions may be useful for work. Moreover, I would not say that all Kaggle competitions are helpful for every project that you face at work. The knowledge that you get at Kaggle is a powerful beast. It brings value only if you know how to tame it.

I use knowledge obtained from Kaggle competitions at work often:

1. If you have a problem in front of you that is similar in some sense to an existing or past Kaggle Competition.
2. If you are able to parse the knowledge that is generated at Kaggle in forums and kernels.
3. If you are able to implement and verify how ideas from Kaggle apply to the problem that you are facing in a fast and hackish way.
4. If you are able to refactor and rewrite your hackish pipelines in a production quality code.
5. If this is the case, Kaggle becomes invaluable.

Not all problems can be represented in a Kaggle competitions format. But in the field of self-driving, there are plenty. In this sense I am lucky. This addresses points 1.

I participated in more than 70 different competitions on various platforms. Not all my attempts were successful, but each of them improved the way I search for information, including Kaggle forums and kernels. And this addresses 2.

There is no way you will become Kaggle Master and not learn how to approach anew, the unknown problem in a fast hacking way with a very high number of iterations per unit of time. This skill in the world of competitive learning is the question of survival :) This closes 3.

4 Is a different story.

One of the reasons why coming from academia to industry was hard for me was due to the quality of the code that I used to write in grad school.

In terms of learning how to write production quality code, Kaggle is close to useless. I do not see how to get this experience except in a company that has a high coding culture and strong Software Engineers that enforce it.

**Sanyam Bhutani**: You’ve rocked quite a few competitions. Which one has been your favorite?

**Vladimir I. Iglovikov**: There are two competitions that I would like to mention. One that is my favorite, and the second one that is the most entertaining.

My favorite is, probably the [Dstl Satellite Imagery Feature Detection](https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection).

1. It was challenging from the engineering perspective There were a lot of nontrivial data transformations in pre-processing and post-processing steps.
2. It was interesting from a scientific standpoint. RGB imagery is well studied, and I would say boring, but RGBD, which contains higher wavelength channels is much more exciting.
3. The problem did not reduce to modification of the fit_predict. Some classes, like water, were better identified in an unsupervised way, based on the physical properties of the material. I do not remember details, but I think there was something about specific heat and infrared light.
4. It was the first challenge when I won a cash prize. My way of thinking changed from “only very experienced participants win top prizes” to “I can do it, what is the next problem in which I can check this assumption?”
5. I bought the second GPU and finally realized that I do not want to deal with Keras + tensorflow till they address my pain points and that it is the time to switch to PyTorch which addressed at least some of them.

Among 70+ competitions that I worked on, there is another that I distinctly remember.

The challenge by itself was not that exciting, just an object detection in aerial imagery, but the story surrounding it was nice. I got to the main page of the biggest Russian internet site [lenta.ru](https://lenta.ru/news/2017/05/22/iglovikov/), and for one day was shown all over Russian TV Channels.

{% include video id="M7wpH4xwBIQ" provider="youtube" %}

The story is a bit anecdotal. I wrote a detailed description of what was happening in Russian in a blog post at [habrahabr.com](https://habr.com/ru/company/ods/blog/330118/) If you speak Russian, you may enjoy it :)

The short version of the events in English sounds like: ”Defense Lab for MI-6 in Britain organized an international competition for object detection in an unknown city in Britain.”

The rules of the competition were very unconventional and this what added the most spice to the situation:

> Everyone can participate, but only the citizens and residents of a particular set of countries can get prize money.

Even though I am a resident of the United States and pay taxes here, I am not eligible purely because of the color of my passport.

The way that these countries were chosen is also interesting. The organizers took some shady corruption rating of countries from 5 years before the competition and put a threshold at some level. Why this level was chosen is also unclear. I like to think that this cut was selected randomly, but my friends suspected that it was a conspiracy in which Britain cut countries it considered as second class citizens, i.e., Russia and China. I hope that it is not what happened, but the cut was just above these countries.

Anyway, I knew about this rule, and I still participated. New knowledge, new pipelines in my private repo - this is important. Prizes are also valuable, but secondary. In this competition, I also had the opportunity to learn from [Sergey Belousov](https://www.linkedin.com/in/sergei-belousov-23925565/), who is not very publicly known Deep Learning expert, who provided mentorship during and after the competition.

I did a few iterations, checked many ideas, implemented a strong object detection pipeline and finished second….

Concerning the rules, I did not deserve the prize, but the fact that the rule exists does not mean that I like it.

Anyway, I wrote posts at Facebook and on Twitter that I am not a big fan of these rules.

The story is spicy and relatively toxic:

“Artificial Intelligence,” “Competition Winner,” “Poor Russian citizen,” “cruel British Defence Lab”, “Accusation of Russia as a country in corruption” and all other fancy words one can exploit in the publication.

Different media outlets barraged me asking for an interview, but all of it was so new to me that I baled. It did not stop the journalists, so instead of talking to me they showed my profile picture from Facebook and Github and invited some strange experts to share their opinion on the topic. Today I would behave differently. I am now more comfortable speaking on camera, and I still believe that information flow in science and engineering should be maximized.

If we want to travel to Mars or extend our life span soon, we need to be more open to the information flow in the scientific and engineering communities.

A big tech company, Mail Ru Group, agreed to pay me the prize money, it was $15k, but I did not feel that I deserve them, so I [asked to transfer them to a fund that supports theoretical Physics](https://paperpaper.ru/papernews/2017/05/23/iglov-science/).

The most hilarious part was when the journalists approached my parents. My mother and father said that although they were an essential part of my childhood, it would be unwise to underestimate the influence of my schooling and that my school teachers are much better candidates for an interview. And it worked :) My school teachers also appeared on TV.

**Sanyam Bhutani**: What kind of challenges do you look for today? How do you decide if the competition is worth your time?

**Vladimir I. Iglovikov**: As I mentioned above, it works best when the challenge is highly correlated with day to day tasks that I am facing. So this is the first type of problem I look for.

Next, I look for problems that are interesting, but farther outside of my comfort zone. For instance, GANs are a bit more foreign to me than I would prefer. Therefore I would definitely participate in the next Kaggle competition on this topic.

The last one is the simplest. There were three competitions at Kaggle in 2017 with $1,000,000+ prize money. I am relatively well paid, so money is not the most essential part of my motivation. But I am open to discussions for advisory board positions in early-stage startups and interesting full-time positions that will add +30% to my total cash compensation. This fact makes me feel that I will give a shot to the next challenge with a good prize.

**Sanyam Bhutani**: How do you approach a new competition? What are your go-to techniques?

**Vladimir I. Iglovikov**: For every ML problem that I face, the first thing that I try to do is to map the data into prediction and prediction into the validation score.

It may be something that I implement from scratch which works well if it is a problem I am familiar with. But if the problem is new to me, I just copy paste from a forum on Kaggle or `git clone` from a relevant repo. If I understand what is happening in that absorbed code this is good. But if I do not have the slightest clue of what is happening it is still more than fine.

In the first stage, I need a reliable baseline, even if do not fully understand all details of how the pipeline work.

In general, for myself, I divide every Kaggle competition into two main stages:

1. Kindergarten stage. It involves reading forum, reading papers, taking relevant classes, doing exploratory data analysis, training a model.
2. Adult stage: I have a pipeline that maps data into cross-validation score and into the submission in a proper format.
This division into Kindergarten / Adult phases is a bit harsh, and you may have a different way to think about it, but I like being harsh to myself. This slightly boosts my productivity.

As Mike Tyson said:

> Anyone who has ever been in a fight knows this is true you can plan all you want, but when punches start to get thrown, plans quickly fly out the window.

In terms of Kaggle competitions, you will overestimate your skill and you will underestimate the talent of the people that you compete with. State of the Art approaches that you presented at Tech Review at work in PowerPoint and that was warmly welcomed by your coworkers will suddenly perform much worse when it is actually implemented in Python and verified on the leaderboard. Drivers, libraries, model and data versioning (Here I would like to mention a tool [dvc.org](https://dvc.org/) that I use for model versioning tasks), the quality of the data, all these and 100500 other small but annoying things will attack you. By default, you do not know where the most prominent issues will be.

Thus the pipeline that moves me to the adult stage of the competition is the first thing that I need to do.

After the pipeline is done, you will be able to do fast iterations. I would like to remind you that the number of ideas that you try is often proportional to your standing on the leaderboard. Thus to maximize your score, you need to maximize the pace of your iterations.

Once I start iterating:

1. I am forced to refactor the pipeline to make it more modular. (Say, for all my computer vision deep learning pipelines I use Remi Cadene’s library, which allows quick checks for different backbones. Same with the flexibility in augmentations, and again, I would like to mention Albumentations library that my collaborators and I are developing and that helped me and many other people to get good results in Computer Vision tasks.)
2. I need to understand my code base better. As I have said, if the problem is new, it may happen that my pipeline will work and produce a good result, but my knowledge of the codebase will be limited. First, I can delete everything that is not used. There may be plenty of the dead code. I delete it. Less code => less bugs. Most likely there is functionality that I do not need => I delete it. Running flake8 or similar tools would be a good idea. Fixing flake8 errors will slightly improve the code, and in the process, I will understand the codebase better.
Renaming variables from **h**, **w**, **i** to something more meaningful as **height**, **width**, **batch_id**. This is small, but it helps. I use PyCharm for my coding in Python. It has all the required functionality for fast refactoring, but I believe that other IDEs are equally good. But! I do not aim to understand the code fully. It will come. My goal is a good model score, and good code quality is secondary. Good code quality for the competition is a nice bonus that helps to iterate fast, and not more than this. For sure, when I will need to share the code within a team or reuse it for another problem, it will become critical and I will spend time on refactoring and writing documentation, but if it comes, it will come later.
Chances are high that I will dump this pipeline or huge parts of it because I will find new ways of dealing with the problem.
3. Get ideas from Kaggle, papers, classes, discussions, and implement them. The goal of fast iterations is to fail fast and do the next step more intelligently.
4. I want to emphasize that ML competition in which you work by yourself and develop code that will be scratched is not the same as developing ML models for production at your job.

Being able to check ideas fast is important, but nothing of the low code quality should be even considered to appear in the production code base at work.

**Sanyam Bhutani**: For the readers and noobs like me who want to become better kagglers, what would be your best advice?

**Vladimir I. Iglovikov**: I would say for those who have not yet tried to participate in Kaggle competitions, but are willing to invest the time to boost your data science skills, to start as soon as possible. If you know the basics of Python and have no experience with ML - this is good enough to start. Just do it, and it is better to do it now than later. Every day that you are thinking about participating but not doing it — there is the knowledge that you do not get.

**Sanyam Bhutani**: Your Carvana competition win involved some HUGE computing resources-which indeed were the needs of the competitions.

Do you feel, in general-a noob could do well in a competition with starter hardware?

**Vladimir I. Iglovikov**: I would say that having GPUs is helpful. And this is true that our team had around 20 relatively powerful GPUs. Hardware helps with iterations, some heavy Deep Learning models may require both hardware and time, and pretty often you may exchange hardware for time, which leads to fast iterations and, as a result, to more knowledge per time and better results.

If you can afford a machine with 2 x 1080Ti, go for it. If your manager at work may allow you to use some of the work computational resources for competitions, talk to her/him about it. Typically, managers are pretty open to you spending your free time and company computational resources on your self-development. Especially if it improves your productivity and you bring novel ideas in-house.

At the same time, I am not sure that a participant with four GPUs has higher chances for success than a person with only two, at least concerning the problems that I have seen so far at Kaggle.

I will give you a couple of examples:

Kaggle Master, [Victor Durnov](https://www.linkedin.com/in/victordurnov/), who finished first in [Spacenet 4](https://medium.com/the-downlinq/the-good-and-the-bad-in-the-spacenet-off-nadir-building-footprint-extraction-challenge-4c3a96ee9c72) was part of the winning team in the [Data Science Bowl 2018](https://www.kaggle.com/c/data-science-bowl-2018) and was also at the top of plenty of other competitions started without any GPUs. He used free credits from Google Cloud. Now he has four Titan V CEO edition that he got for the Data Science Bowl 2018, and I am pretty sure that he likes it more than using the cloud.

In his [interview](https://hackernoon.com/interview-with-kaggle-grandmaster-senior-cv-engineer-at-lyft-dr-vladimir-i-iglovikov-9938e1fc7c), [Artur Kuzin](https://www.linkedin.com/in/n01z3/) spoke on how Kaggle Master [Valeriy Babushkin](https://www.linkedin.com/in/venheads/) got his first gold medal in a Computer Vision / Deep Learning competition without having GPUs. He got a strong result with CPUs at the beginning of the competition, and many people with GPUs were happy to merge in a team with him. I would say that there are plenty of people who want to participate but do not have GPUs, and plenty of those that have GPUs but are less motivated. Show show some result, and people with hardware will appear.

**Sanyam Bhutani**: You’re an active member of the ods.ai community. Can you tell us more about ODS? We can see many teams from ODS in the Top LB(s), are noob kagglers welcome in the community as well?

**Vladimir I. Iglovikov**: It is more than this. If you look at [my LinkedIn](https://www.linkedin.com/in/iglovikov/) there is a line of me being an evangelist for ods.ai as a community. I believe that the community is excellent, and it boosted my ML skill a lot. It took me a couple of years to get my first gold medal at Kaggle when I was competing on my own. I joined ods.ai and other top finishes came much faster :)

[ods.ai](https://ods.ai/) is a Meritocratic Russian Speaking Data Science community. At the moment it is about 30k members. Not all of them are active, but there is a significant number of people that are there pretty regularly and have Data Science as part of their lives. It can be for research, competitions, education, pet projects, business-related initiatives, and anything else. Everyone, except for the representatives of the Human Resources departments, is welcome. Some people are making their first steps in Data Science, some people work more on the research side, others make money for building products with Data Science techniques as I am. Basically, everyone who is excited about Data Science and is willing to learn DS in an efficient but probably the hard way is welcome.

The most significant part of the community lives in the former Soviet Union, but there are plenty of people from the US, China, Europe, Canada, and India. As long as you are excited about Data Science, it is an excellent place to be. The right place to ask a question, the right place to give an answer.

There are a few initiatives that were born in ods.ai

* [DataFest](https://fest.ai/) —the most significant Russian Speaking Data Science conference. Influential speakers, support from the biggest Russian tech companies. Special thanks to Alexey Natekin and team for organizing. There is also Minsk DataFest, I was a keynote speaker there last year, which is organized by Arseny Kravchenko.
* [mlcourse.ai](https://mlcourse.ai/) — Russian / English online ML class that was created by Yury Kashnitskiy and team with the motto: “learn ML the hard way.” Really good. I recommend it.
* [dlcourse.ai](https://dlcourse.ai/) — Deep Learning course by Simon Kozlov, who felt that knowledge that he has in the domain of Deep Learning should be shared with the students in his alma-mater Novosibirsk University and is teaching the class online. He is even flying to Siberia for a final exam :)
And many others participate, like Kaggle Masters [Valery Babushkin](https://www.linkedin.com/in/venheads/) and [Alexey Grigoriev](https://www.linkedin.com/in/agrigorev/) who write books and publish online courses about Data Science.

I would like to emphasize that these people spend their time improving the state of Data Science knowledge, without pay, purely because it is the right thing to do. This philosophy is consistent with many facets of the ods.ai community.

**Sanyam Bhutani**: Given the explosive growth rate of ML, How do you stay up to date with the State of the Art Techniques?

**Vladimir I. Iglovikov**: I do not. And am not even trying. The field is too broad. When I have a problem that I need to solve, I dig deep into the latest achievement in this particular area. For the topics for which I do not have hands-on experience, my knowledge may be minimal. I am trying to work on a few diverse problems at the same time, a couple at work, a competition, and a pet project, which gives some breadth of view. I have hope that I am experienced enough to be able to pick a new topic, say voice recognition, and become proficient with expediency.

Reading the latest papers on all topics from morning till evening is a pretty bad idea. Life is too short and valuable for this type of activity.

I read papers daily, but only for the problems that I am facing. Also, I analyze the winning solutions to different competitions. As we discussed above, it is an invaluable source of information, if you can parse it correctly.

Attending conferences like CVPR, ICCV, as usual, works really well. Dense, exhausting, but a very productive way to catch up with the field in general.

**Sanyam Bhutani**: What progress are you really excited about in Computer Vision?

**Vladimir I. Iglovikov**: In terms of papers, my latest favorite trick is to use siamese networks for image classification and tracking, where you do not learn class values, but class embeddings.

I really like the concept. But I also like how it allows using a small amount of data for training.

My guess is that to move in the direction of general artificial intelligence, robots, self-driving cars being a product, and other exciting sci-fi areas we, probably, need to figure out how to use the existing data more efficiently. And in this sense, I like siamese networks and overall work that the community does in the direction of one-shot learning.

**Sanyam Bhutani**: Do you feel ML as a field will live up to the hype?

**Vladimir I. Iglovikov**: Being honest, I do not know. Let’s rephrase the question.

There are plenty of people that go to college to the Computer Science department for four years, thinking about going to Graduate School for five years, so that in 4 + 5 = 9 years they will have an interesting, well-paid job in the domain of Machine Learning. I am not sure that they will. But we will see how it goes. Everything is changing too fast these days :)

**Sanyam Bhutani**: Before we conclude, any tips for the beginners who feel overwhelmed to start competing?

**Vladimir I. Iglovikov**: There is only one piece of advice for those who want to start competing. Just do it, and try to get to the top, learning from everyone and everything. Kaggle is a great learning environment for a big subset of Machine Learning skills. The earlier you will start, the earlier you will acquire them.

Sanyam: Thank you so much for doing this interview.

**Vladimir I. Iglovikov**: Thanks to you for organizing it and everyone who will have the patience to read till the end :) And special thanks to [Erik Gaasedelen](https://www.linkedin.com/in/erikgaas/) for proofreading!

Edit: Thanks to [Yury Kashnitskiy](https://www.linkedin.com/in/kashnitskiy/1) for proofreading and suggesting a few corrections.

Edit2: Many Thanks to [Tatiana Gabruseva](https://www.linkedin.com/in/tatiana-gabruseva-phd-a2383315b/) for further proofreading.
