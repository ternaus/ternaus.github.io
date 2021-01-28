---
layout: single
title:  "I want to organize ML competition. Where is the playbook?"
excerpt: "Organizing ML competions is not hard. Still, companies do not do it well."
categories: kaggle
tags: kaggle tutorial

header:
    teaser:
    og_image:
---
{% include toc title="Table of Contents" %}

There is no such a playbook, but there is a standard set of mistakes that organizers make.

You may think about ML competition as an exchange.

You provide:
* **Human Resources** to organize the competition.
* **Prize money**
* **Intellectual property** in the form of the data.

and expect to benefit in technical, hiring, and marketing domains.

* **Technical**: improve production ML models.
* **Hiring**: you will get access to the pool of skilled candidates.
* **Brand awareness**: more people will know who you are and what problems your business solves.

To be clear. You will invest money and human resources. Insights from the competition could be used by your competitors. Still, there is no guarantee that your company will benefit in any way.

Competitions provide opportunities, but it is up to you to use them.

And, of course, the better you organize the challenge, the more options you will get.

A better organization does not mean investing more money or human resources. It means avoiding mistakes.

It is trivial to organize "some" competition. But I hope that "some" is not your level and that you are shooting for a great one.

In the article, I will describe topics that organizers need to keep in mind. The text consists of small subtopics; you can read them independently.

It is a "longread" and unlikely that many people will read till the end. But I hope that future organizers will consult with the text when they work on their own challenge.

## Compass

From the first day, you will encounter questions like:

* Where to host? Do it yourself or use a third party?
* What is the format of the data?
* How to promote?
* Should we allow participants under 18?
* etc

I recommend the following compass to guide your decisions:

> **Every time you make a choice try to maximize the number of participants**.

A participant is a person who made a submission at appeared on the competition Leaderboard.

Suppose a person downloaded the data, made an extensive exploratory analysis, read 100 relevant scientific papers, hosted 10 webinars on approaching the challenge but did not appear at the leaderboard. If you want, you can call him an "influencer," but definitely not a participant.

The number of participants is a straightforward metric that is easy to measure. When you optimize it, all other metrics will go to the "green zone" automatically.

Quality of the competition vs. the number of participants:
* **Bad**: 0-10
* **Ok**: 10-100
* **Good**: 100-1000
* **Great**: 1000+

For sure, not all participants are equal. One person will spend a few hours and forget about the challenge.
The second will work on the problem 24/7, sharing valuable insights with others at the forum.

It is not that important. The compass is not about the specific numbers but about **the order of magnitude**.
When the engagement increases 10x, absolute numbers for all categories of participants go up.

## Human Resources

At a minimum, you need two people:
* **Technical**:  engineer or scientist
* **Non-technical**: product manager or marketing person

They will work on the problem part-time, but there should be clear owners for various parts of the project.

Besides, the project needs support at the director level. You will have requests from other teams, and you need a decision-maker that will help you.

## Find an advisor
Competitive machine learning is different from machine learning in industry or academia. Some things that you assume are crucial are not important at all. Others, looking non-relevant, would be worth thinking about.

Look within a company. There may be a person in another department who organized or participated in the ML challenges before. Involving such a person as an advisor could save you a lot of time and energy.

**Example**: In 2019, Lyft Level5 planned to organize an [ML competition on the perception dataset](https://www.kaggle.com/c/3d-object-detection-for-autonomous-vehicles).
I got involved in the project by accident. Stopped to grab a coffee in the kitchen and got into a morning chat with a person driving the effort.
I shared what I learned during my career as a professional competitor. He asked me to join the team of organizers.
Based on my feedback, we adjusted a few things. I hope this made the challenge better.
{: .notice--info}

## Understand the participants. Who are they, and why do they compete?

Your motivation as the organizer is different from the motivation that your participants have. I recommend understanding who the participants are to make your incentives aligned.

You want the challenge to have a positive impact on your business. Participants do not care about your company, its mission, and how the competition will affect your business.

Working on ML competitions is a second, unpaid full-time job. You need very good reasons to invest your free time in them.

I like to think about machine learning competitions as about weight lifting gym but for ML muscles.

People wake up early and go to the gym to develop the body and look better, but the main reason is that they enjoy the process. (Endorphins get released.)

The same story here: there are new skills and knowledge, but people mainly participate because it is a lot of fun.

People imagine the typical participant as:
* Wakes up in the morning, full of energy.
* Actively looks on the internet for an exciting challenge.
* Finds one where he has some expertise.
* Ignores her day job, university, personal life.
* Without any guideline or tutorial, figures out how to get access to the data. Through pain, learns how to work with it.
* Writes the code and trains the model.
* Uses her intuition to decipher a poorly written description of the submission format.
* Creates the submission and uploads it.

The reality is different. I would not even recommend thinking about participants as someone eager to work on your problem through the pain.

In reality, the two hours of the challenge look like this:
* The person comes home in the evening, tired from the job or classes.
* She already knows about the competition because she read about it on some blog or got an email about the competition announcement.
* She chooses to work on this problem because the challenge looks interesting. She does not know how to solve it, but it is her chance to master the task.
* She downloads the data and tries to write an end2end pipeline.
* If she does not understand how to approach the task, she gives up and never comes back to the problem.

Think about participants as your clients. You want to maximize their number and engagement, and you do not want to lose them to the competitors.

Many ML challenges happen at every moment. If you do not treat yours seriously, others will be more interesting, have larger prizes, and better organization. Participants will go there.

**Recommendation**: Participants should feel the least amount of friction possible.
{: .notice--danger}

## Do not host yourself. Use third-party.

Most of the ML challenges follow the path:
* Find $1000 for prize money.
* Find an intern or graduate student. Tell her to prepare the dataset, introduce the metric, and define competition rules.
* Announce the problem in the post on the company's blog.
* Ask participants to send predictions by email. Intern will evaluate them manually.

When the competition is over, split $1000 among winners, call it a "Great success."

Most of the ML challenges that happen in conjunction with academic conferences follow precisely this path. This was also the original plan for Lyft's 2019 challenge.

Such competitions have 0-10 participants. This is bad.

I participated in a few such challenges at  CVPR and MICCAI. My team got to the top in all problems that we tried. Weak participants and the whole process is not very enjoyable.

Ideally, you want:
* Thousands of people working on your problem
* Insights are generated through the whole challenge and not only at the end.
* Participants have access to hardware even if they do not have powerful desktops at home.
* Scores are computed automatically, and the leaderboard is calculated automatically.

Competitive machine learning is a maturing field. Many companies provide platforms for challenges: Kaggle, Topcoder, Datasoluls, Drivendata, Aicrowd, Signate, etc.

I am not affiliated with Kaggle. But I believe that Kaggle is the largest and the most established platform. Most of the challenges that I joined as a participant, and both that I organized, were at Kaggle.

If you have enough budget and they are interested in your problem - I recommend working with them. Kaggle is a popular platform that hosted hundreds of ML competitions. It also provides CPU, GPU, TPU hardware to participants.

The representatives of the platform will help avoid common mistakes about your dataset.

**Example**: In 2018, I participated in the Giana challenge (part of the MICCAI conference).
At the end of the challenge, I sent my prediction in email and went rock climbing.
I thought that my work on the challenge is over, but I got an email that there is something with my prediction file,
and the organizer cannot calculate the score. As a result, I was editing my prediction file from the cell phone in the
middle of the Sierra mountains. We fixed the issue, but I did not like the experience. If there is an issue with
my submission file, I need to know it instantly. In 2019 I decided not to participate.
If organizers worked with a platform, they could avoid this issue.
{: .notice--info}

**Recommendation**: Do not try to host the competition yourself. Use one of the platforms.
{: .notice--danger}

## Prize money

What is a good prize money?

There is a correlation between the number of participants and the prize amount. But it is non-linear. For sure, $1000 is questionable, but the difference between $100,000 and $1,000,000 is relatively small. I would not say that it worth an extra $900k.

If your dataset and your problem are bad, a large prize will not help. If it is interesting, you will get good engagement even without huge reward.

**Recommendation**: do not overthink this, assign $25k for prizes, and focus on other more important things.
{: .notice--danger}

## Kaggle tiers and points

One of the features that distinguish Kaggle from other platforms is its gamification system. A small number of people spend their free time on challenges to each money. It is either novice who did not have a chance to measure their skillset or elite competitors who know what they are doing.

Kaggle has a system of tiers:

* [Novice](https://www.kaggle.com/progression#novice)
* [Contributor](https://www.kaggle.com/progression#contributor)
* [Expert](https://www.kaggle.com/progression#expert)
* [Master](https://www.kaggle.com/progression#master)
* [Grandmaster](https://www.kaggle.com/progression#grandmaster)

You get the title based on the medals that you obtain during the challenge: gold, silver, bronze. Getting to the next stage is exponentially hard.
There are only 200 Kaggle Competition Grandmasters out of 3 million who joined and 150k that actively participate.

These titles matter a little outside of the competitive community but matter a lot within.
People spend days and nights to get rare badges in World Of Warcraft and other computer games. The same story here.

Besides, kaggle assigns points to the competitions. Points from all challenges you were part of are summed up.
This tells your place in the overall rating. These points expire with time.
Being within the top 100 out of 3,000,000 feels like an achievement.

(At the peak I was [19th](https://www.kaggle.com/iglovikov)).

By default, Kaggle enables tiers and points for all competitions except those where the organizer cannot guarantee the data's high quality. One of the criteria is that the test set cannot be accessed online.

**Recommendation**: If you work with kaggle, discuss with them the situation with tiers and points.
Points will lead to better engagement. If kaggle disapproves your dataset for the competition with points,
this is a big red flag about your dataset.
{: .notice--danger}

## Competition format


There are three main formats:

### Offline / offline

Participants train and perform inference on their own hardware and send the file with predictions to the platform.

**Pros**:
* Participants will squeeze the most out of the dataset and the problem.

**Cons**:
* Top solutions will be rather complex
* Some teams will perform better because they have access to more powerful hardware.

### Offline / online
Participants train offline on their own hardware and perform inference on the platform's hardware—examples: Kaggle kernels or Docker container submissions at Topcoder.

**Pros**:
* You can restrict hardware and inference time to bridge the gap between the competition and production setting.
* Participants do not have access to the test set. Better check for the generalization of the model.

**Cons**:
* Harder to organize. The platform needs to support this functionality. Example: Kaggle does not support docker submissions.

### Online / Online

Participants train and perform inference on the platform's hardware.

**Pros**:
* You can restrict hardware, train, and inference time to bridge the competition and production setting gap.
* All participants are in the same boat for the train and for the inference. Getting to the top is about skill and creativity and not about the number of GPUs at your disposal.
* Participants do not have access to the test set. Better check for the generalization of the model.
* Participants that do not have their own hardware can join.
* Full reproducibility of the pipeline.

**Cons**:
* Not all potential of the problem and the dataset will be explored.

It looks crucial to choose the best format for the competition, but it is not.

Insights from the winning solutions have at most 30% of the value. The largest (70%+) impact comes from the tricks and ideas that participants generate during the challenge and share at the forum. The format of the challenge is secondary.

My favorite is the offline/online format. It allows to squeeze the most out of the problem, but the inference is closer to the production.

**Recommendation**: Pick a format that you like, and if it does not work for some reason, relax the constraint. It is not a big deal. You'd better focus on absorbing the most from the tricks and insights that the community will generate from the first day of the challenge.
{: .notice--danger}

## Competition Metrics

The leaderboard is computed based on the metric score.
Every problem could be evaluated using various metric functions, for example, for classification tasks: log_loss, Accuracy, Roc_auc score, F1, etc.

I would recommend choosing one that is closest to the production setting.

It may happen that platforms do not support your metric.
They can add any reasonable metric, but you need to discuss it way ahead.

## Dataset

Dataset is the most critical part of the whole story. If you mess it up, nothing will save you.

To host the competition, you will release some of the internal data. The first question is what license to use? I would recommend picking one that allows non-commercial use.

The size of the dataset correlates with the number of participants. There are two edge cases:

The dataset is small. People can train models on laptops—a lot of participants.
Dataset of 10-500Gb. Participants will need access to the cloud or desktop with GPUs. The engagement will be smaller, but it is still quite possible to have more than a thousand people.

Tabular data problems fall in the first category, computer vision, natural language processing to the second.

The difference between 10 and 100Gb size datasets is relatively small. You approach both with the same data processing and training pipeline.

**Recommendation**: Do not overthink this. The size of the dataset is secondary. If you can release more - release what you can.
{: .notice--danger}

### Data format

Participants will take the data in the format you provide and convert it to the form that suits them best. But taking extra steps can feel frustrating and push people away.

**Example**: companies that use Tensorflow like to release the data in the tfrecords format. Do not do this. This is interpreted as laziness and a lack of respect for the community. If the person needs to look at the image in the dataset, she should be able to click on the file, and that is it. If she needs to write code to visualize the photo, it is frustrating.
{: .notice--info}

**Recommendation**: Go with jpg for images, png or RLE for masks, CSV, and json for tabular and text data. Easier to access the data - better. Do not use uncommon formats to make your dataset 10% smaller.
{: .notice--danger}

### Dataset SDK

Suppose your dataset is involved and unfamiliar, as was in both Lyft's competitions. It is crucial to provide an SDK and tutorial that help to work with the data. An ideal situation is if you can open-source the library that you use internally.

We did this in 2020 with [L5kit](https://github.com/lyft/l5kit).

As a result, improvements that participants made from the first day positively impacted similar internal tasks.

While open sourcing the L5kit, we improved it's structure and decoupled it from the internal libraries.
Participants found a bug in the SDK, identified I/O bottlenecks, and proposed ways to address them. I/O improved 6 times.

For the SDK license, I recommend having something permissible like Apache-2, MIT.

You will have discussions with the legal team like: "The license for the dataset is A, for the SDK is B, what license do we pick for the winning solutions?".

If you go with a permissible license for SDK, it will make such discussions faster and easier. At the end of the day, your SDK is just a set of helper and visualization functions. It is not an ultra crazy intellectual property that can give your competitors an edge.

People should be able to install your SDK with `pip install` in one line without any pain. A five-page installation manual is not ok.

Kaggle provides a way to work with the data and train models on their hardware (CPU, GPU, TPU) in Kaggle Kernels. If you work with Kaggle, you need to check if your SDK works in Kaggle Kernels without any problems.

Recommendation: Easy access and visualization of the dataset are ultra-critical. It is more important than the prize value or the size of the dataset. Do not underestimate this!

### Train / test split

As an organizer, you want your model to generalize well. I.e., work well on the data that it has never seen before.

To check the generalization ability of the model, people split into two parts:

* Train
* Test

People train on a train set, perform inference, and evaluate model performance on the test set.

Participants do not have access to the test set labels, and in the case of the (\[offline, online\] / online) format, even to the test set.

Issues begin when the train set and test share common data or at least information.  The problem is called Data Leak.

If you have a data leak:
* How well will models generalize to production is unclear.
* PR risks. Data Leak is considered such a basic mistake that competition with it gets bad PR. The reputation of the company's Data Science team will be affected. It will solidly get attention on social networks.

The thing is that this mistake is not basic at all. Data leaks happen pretty often in industry, competitions, and in academia.

It can take years to find data leaks in the academic dataset (no one is looking at exploiting the data). In ML challenges, it will take hours when thousands of eyes are actively searching for ways to get an edge over other competitors.

If you have a data leak in your data, it is not the end of the day. You can provide a new test set and reevaluate the Leaderboard. Still, it is better to avoid the situation from the beginning.

If you organize the competition at Kaggle, their specialist will help to avoid obvious pitfalls, but do not overestimate their help. They have a playbook about data leaks and how to avoid them, but your task is not their domain, and they can miss non-obvious problems.

Random train/test split is rarely the way to go. Split by patient/geography or time will serve you better.

**Recommendation**: Pay close attention to the way you perform train/test splits. It is better to avoid Data Leak in the first place rather than deal with the consequences.
{: .notice--danger}

## Sample Model

After the participant appears at the Leaderboard, she is hooked. The dopamine gets in her blood, the focus shifts from critical tasks at her day job to the ML challenge. From now on, she will work on the challenge, replacing old modules in her pipeline with new ones that she will learn in literature and her own creative mind.

As an organizer, you need to ensure that this actually happens. This is consistent with our compass: "maximize the number of people at the leaderboard."

It is easy to do. You need to provide a code, called sample submission that:
* Processes the data
* Trains the model
* Evaluates the model using cross-validation
* Performs an inference
* Generates the submission in the correct format

There is no need for this submission to be ultra-accurate. The most important part is to ensure that it runs and that people can run it even if they do not understand what is under the hood. They will learn it, but later. It is much easier to understand the flow when you have an example in front of you.

Your sample submission will also affect where participants will invest their resources in the first month of the competition. Hence, if you are curious about how an algorithm from the recent conference that claims to be state of the art perform on your dataset - just write a sample submission based on this algorithm.

Recommendation: It is better to have a sample submission on the first day of the challenge. Sample models for straightforward datasets will not provide a lot of value. Participants will create such models and share them with the community. If you explore the new type of task and involved dataset, a sample model can drastically decrease the friction and boost the engagement.

## External Data and pre-trained models

More data is better. Some techniques do not work on small datasets. You want to know how the amount of train data will contribute to the model's accuracy.

As an organizer, try to provide as much training data as possible. If participants do not have powerful hardware, they will use the subset of what you provide.

There is another way to enrich the problem.
Datasets from similar tasks. This is popular in medical imaging contests where datasets are limited.
Pre-trained models. People train model on dataset A, publicly share weights of this trained model, participants use these pre-trained models in their solutions.

In many competitions, organizers allow external data. But things can go wrong, and this is related to the legal.

Classic story - Researcher takes the dataset that DOES NOT allow commercial use, trains a model, and shares it publicly using a license that ALLOWS commercial use.

The question is - can people use models that he trained or not for commercial purposes? Model is not data; it is a derivative of the data. It contains the information from the original dataset in aggregated form. There are examples of when the original data was extracted from such trained models.

Deep Learning frameworks by Facebook (Pytorch), Google (TensorFlow), Intel (OpenVino) provide a set of pre-trained models. Many of these models are trained on datasets that DO NOT allow commercial use. The most prominent dataset is ImageNet.

I created issues at Github regarding this question and asked companies to clarify the models' license in their libraries.

* [Pytorch](https://github.com/pytorch/vision/issues/2597)
* [Tensorflow](https://github.com/tensorflow/models/issues/9131)
* [OpenVino](https://github.com/openvinotoolkit/open_model_zoo/issues/1433)

The best answer: "We do not know. It is up to your legal department to calculate the risks of using our pre-trained models."

You can interpret this as companies that use pre-trained models could be subject to a lawsuit. And this is 99.9% of the companies that use computer vision.

Concerning the competition, this means that the organizer wants models or some parts to be used in production. Hence you would like to limit data and pre-trained models to the set that allows commercial use.

Typically, at Kaggle, there is a thread at the forum where participants post links to the datasets and pre-trained models they plan to use. They ask for approval from the organizers. But!

* Kaggle representatives cannot answer this question because it is up to the organizer.
* The researcher/engineer that organizes the competition cannot answer it because it is a legal question.
* She pings the legal department. They are busy, and the situation about competitions / pre-trained models is unfamiliar to them.
* They set up a meeting in a few weeks to discuss the situation.
* Legal gets the idea during the meeting, but they need to have a follow-up meeting in a week.
* In the follow-up meeting, the legal team does not say: "Yes, they can use," "No, they cannot use." They instead talk about potential risks in either of the ways.
* Now, the Researcher needs to take responsibility and publicly verify: "Yes, it is allowed," "No, it is not allowed."

In practice, participants will post in the external data thread, the host never replies on what is allowed and what is not. Participants assume that it is ok if they posted in the thread, but it could not be the case.

Similar situation with datasets.

Example: In the winter and spring of 2020, Facebook hosted the Deepfake Detection Challenge, the prize was $1,000,000.

External data and pre-trained models were allowed in the competition. Participants posted links in the external data thread.

Hosts did not want to take responsibility for the decision. They gave inconclusive vague responses.

As a result, the team who finished first and was already splitting $500,000 in their mind was disqualified. External data that they used and posted at the forum was not allowed. Still, they learned this only after the competition was over. The community was not happy with how the Facebook team handled the situation.

How to deal with this?

You will not use models that competitors trained in production ever. At most, you will take their code and train on your in-house datasets. Hence it is not really crucial if external datasets or pre-trained models could be used for commercial purposes. Allow those that you like, and do not overthink this.

The only exception is if the team uses a codebase that does not have a permissive license.

**Example**: YOLO 5 is a powerful modern Object Detector. It's [Pytorch implementation](https://github.com/ultralytics/yolov5) has a GPL3 License,
which does not allow commercial use. In one of the Kaggle competitions top team used it as a part of their solution. They were disqualified.
{: .notice--info}

The deepfake story happened due to miscommunication and the lack of transparency.

This was [well-received](https://www.kaggle.com/c/lyft-motion-prediction-autonomous-vehicles/discussion/199829):

![](https://habrastorage.org/webt/w7/f_/md/w7f_mddr-jeyinv6yjwbho6-th0.png)

Pre-trained models and external data is just a nice addition. If you will not allow them but will make this point clear, no one will get upset.

**Recommendation**:
* Do not overthink the value of "commercial use only" pre-trained models and external datasets. It is not really important. Allow as much as you can, as long as all participants have free access to it.
* Discuss it with your Legal department that this is ok to give the host (engineer/researcher) a right to say "Yes" and "No" about external data and private datasets without consulting with Legal.
* State clearly in the "External data thread": "If the host did not say explicitly yes, this is allowed. It is not." Here is an example of the thread that I created for Lyft's 2020 competition.
{: .notice--danger}

## Support during the competition

After the competition launch, you need to provide support. It takes at most 30 minutes a day. Typically much smaller.

You will need to address things like:

**Technical**:
* What does X in the dataset description mean?
* I think there is a bug in the metric; I think this happens because of YYY.
* There is a bug in the dataset SDK. Here is proof.

**Non-technical**:
* Can underage people participate?
* Can we use the dataset outside of the competition?

Some competitions may have drama:

Participants will find a bug in the metric or Data Leak. You will need to address the issue and restart the competition.
Someone copy-pastes the code from someone without giving them credit, and somehow it ended with a heated emotional discussion.
Someone unskilled pays a strong team to join them and get Kaggle medals/points without working on the problem.

In 2019 I answered all types of questions.

In 2020 we had more resources, and Luca Bergamini and I split the responsibilities.

Luca works on the motion Prediction tasks at Lyft Level5. He understands the dataset, metric, SDK, and all technical nuances better than me -> he was covering technical questions.

I took care of the non-technical and was prepared to partner with the Kaggle team and resolve all the possible drama.

**Recommendation**: The person that works on the problem internally must cover technical questions.
* His answers will be precise and informative, => a better user experience.
* He will learn from the participants. Only 30% of the value comes from winning solutions. 70% is coming from the forum. It is a separate world with its own slang. To absorb all of the information, you need to know the problem well and spend enough time communicating with participants.
{: .notice--danger}

## How useful winners models to the production?

There are two opposite opinions:

* Winners dream of writing their solutions in the production quality code, with good documentation and using only those libraries that will allow the organizer an easy integration.
* Winning solutions are absolutely useless. It is always an ensemble of the models that are very far from the production setting.

Let's look at what is right and wrong about them.

Participants care only about one thing - the score on the Leaderboard. They will overfit the dataset and the metric, fighting for the improvement in the 5th digit after the decimal point. The final standing of the participant is proportional to the number of ideas she tries. The majority of the code she writes will be scratched. The most important thing - is how fast do you iterate. The quality of the code is secondary. Winning solutions will be far from production quality.

Participants will use tools that are the best for strong models and fast iterations. How easy it will be for you to integrate the solution will not cross their minds.

**Example 1**: Until 2020 Lyft. Level5 used Tensorflow in the car. Participants of Lyft's 3D Detection challenge used Pytorch.
{: .notice--info}

**Example 2**: There were challenges where organizers encouraged participants to use MatLab. Matlab has a niche where it is the best language and set of libraries, but it is not machine learning. All the encouragement was ignored.
{: .notice--info}

Every idea that the participant tries is a separate submission. They will pick the best, or you can combine them in an ensemble. Ensembles have slightly better accuracy and have better generalization ability. Everyone builds them. This ensemble is slow and heavy, far from the production setting.

But! Ensembles add just a little on the top of single models. The winning solution is not a combination of similar weak models. It is a combination of strong, diverse models. Typically the best single model from the ensemble is also a top solution.

**Example 1**: Carvana Challenge. Our ultra-heavy ensemble finished 1st. But single models were in the top 10.
{: .notice--info}

**Example 2**: Lyft Motion Prediction Challenge. First place used a complex ensemble, but the best single model would also finish first.
{: .notice--info}
Code from winning solutions will be hard to integrate into the production. You will need to understand what is happening in these solutions, take useful ideas, and rewrite them, following your internal coding guidelines.

**Recommendation**: You will not deploy winning solutions to your production as is. I recommend having a person that works on the competition problem internally as a part of the organizing team.
{: .notice--danger}

## Marketing

Should you invest in the promotion of your competition? Of course. If you do not do this, the number of participants will be smaller. That is against our compass.

People need to know:
* that your challenge is happening.
* That problem is interesting
* That the entry point is low even if the problem is novel and ultra-complex.

Things that we did in 2020:

* We hosted at Kaggle, and Kaggle sends an email to 3,000,000+ people at the launch of every challenge. These people are related to ML. Most of them tried at least the tutorial competition.
* We released the train set months before the challenge, published a blog post, and encouraged people to use it in their research. The goal is to engage the academic audience.
* We wrote a pre-print about the dataset and published it to ArXiv. Later we submitted it to the CoRL conference. Our head of AV Research presented the paper there.
* We organized two webinars, one as a part of the ECCV, where we talked about the dataset and the challenge. I was surprised, but we got hundreds of participants, and they asked the right questions. Later we published Q/A based on it.
* Social Networks: LinkedIn, Twitter, Reddit, HackerNews
* We applied to host the competition as a part of the NeurIPS competition track (we were rejected). Could give more attention to the academic audience.

I would say that the most impactful point is [1]. Everything else had some value, but my guess that it was not very large.

Do not be shy about marketing. You invest time, money and resources. You help with the democratisation of AI.
Many people will start their journey to the world of machine learning because they will feel excited about your ML challenge.
It is ok to be proud of this, especally if problem is interesting and organization is at the high level.

## Hiring

During the competition, you can see how well participants perform on your problem and consider hiring them.

In theory - it is an excellent opportunity to evaluate candidates, but it does not work well in practice.

**Geography**: Many candidates live in the former Soviet Union, India, and China. You could be interested; they could be interested. But the situation with visas makes it hard to happen.

**Expectation mismatch**: Elite competitors do not have problems with work. Most likely, positions that you have will not interest them.

**Example**: My friend [Selim Seferbekov](https://www.kaggle.com/selimsef) participates in competitions to earn money. Last year he got $500,000 in the Deepfake challenge. After taking 6 months break from it, he got prizes in 7 other challenges—standard ML positions in Google, Facebook, Lyft to him look ultra boring. At the same time, he would be happy to explore options at Deepmind or another company that "works at the edge" and has an excellent financial component.
{: .notice--info}

What about non-elite competitors? Are they good? They are great. But recruiters rarely look below the first three places.

To get a job, candidates need to pass resume screening and a set of interviews. Candidates with a competitive ML experience are so rare that recruiters are not used to the keywords they add to the resumes. For example, "Kaggle Grandmaster" will not mean anything to them.

There is an exception. In the internal doc for HRs at Facebook, "Kaggle Master" is treated as keywords that deserve attention.

Even if they pass, most of them will perform weaker than other candidates during interviews. Your team will not be able to evaluate her strengths, and she will not perform well on things you ask from an average candidate.

**Example**: A number of my interviews followed the pattern:  I was told that my ML knowledge is impressive, and no need to waste time digging deeper into this. Instead, I was asked questions about algorithms and data structures. I remember, in one company, it was LRUCache. I had no slightest clue what it is and how to implement it. I did not pass.
{: .notice--info}

Some companies figured out how to hire people from competitions and make them bring value. For example, H2O.ai, Nvidia, Deepmind. But it is an exception. You may contact hiring teams in these companies and ask about their ways.

There are secondary effects that help with hiring. With the competition, you broadcast what problems do you solve. This makes people who like these tasks excited. During 2019, 2020 Lyft's challenges, participants messaged me and asked about Lyft, Level5, what problems we solve, and how to become a part of the team. We do not have a particular hiring pipeline for this case; I passed their resume to HRs and did not follow after.

**Recommendation**: Look for people in the top 50 and not the top 3. Think about candidates as Research Engineers and not Research Scientists or Software Engineers.
{: .notice--danger}

## Wrapping up

After the competition is over, I would recommend:

* encourage people to share their approaches at the competition forum.
* writing a [blog post](https://www.kaggle.com/c/3d-object-detection-for-autonomous-vehicles/discussion/133895) that summarizes insights from the challenge.
* organize a [webinar](https://zoom.us/rec/play/dOoHuXMhrF6UIkSlV8DMl44mZrNyi0sgAH7_kLveLwkWw9AANTQfcOocGaQbDZufQl6Ys2J8ZJboiIA-.-9eGyvScLNs2wuHg?startTime=1611680449000&_x_zm_rtaid=aFmsdeu0RHW3GdXWe5Dx4g.1611701532489.5e61e2b6b6466cf80494f3b1a7d17f3d&_x_zm_rhtaid=796) where winners can share their techniques and answer questions from the community.
