---
layout: single
title:  "More hardware to the participants in Machine Learning competitions!"
categories: review

tags: machine_learning kaggle

---

This article was originally posted at [Medium](https://medium.com/@iglovikov/more-hardware-to-the-participants-in-machine-learning-competitions-b31fc4ebdef5).

---

Hardware in Machine Learning competitions is not everything, but having a good machine helps.

I like Google Collab, I like Kaggle kernels, and I love that Amazon and Google provide credits fro AWS and GCP for the participants in competitions.

I want to share one more initiative in this direction.

[Hostkey](https://www.hostkey.com/) is a web service provider.

They have a [program](http://landing.hostkey.com/grant_for_winners) in which the competitors in Machine Learning challenges(ML) with a prooved record of getting to the top in competitions may get a dedicated server with GPUs to use on the problem.

> We offer free GPU servers to the winners of grants at large competition venues for their use in further competitions, for training or for personal projects related to data science.

The deal is:
* The participant gets a server for free, but he/she needs to give feedback on the product.
* The participant will need to write about the experience in social media. That is what I am doing in this blog post.

I started looking at the [DeepFake challenge](https://www.kaggle.com/c/deepfake-detection-challenge). The dataset was around 500Gb of videos. Processing the data and training models on the dataset takes a decent amount of time.

When I realized that cropping every 10th frame takes forever on my desktop, I upgraded the CPU to [AMD Ryzen Threadripper 3970X](https://amzn.to/32zQVEk) and added fast [SSD 970 EVO 2Tb](https://amzn.to/3jlao2k). This helped with the preprocessing, but for training, I needed GPUs.

Luckily Hostkey the program and after my request provided a server with 8x1080Ti for the duration of the competition.

Did everything work instantly out of the box? Of course not :)

The server worked, but initially, I was not able to unpack the dataset.

The issue was that the file system at disk was “ext3”. For everyday work that you do at the computer, you would not care, but when you work with many files, this may be an issue. “ext3” was released in 2001 and at that time people did not expect that the user will routinely work with hundreds of thousands of folders and million files.

Remember, “640K ought to be enough for anyone.” that people believe Bill Gates said in the early 1980s? :)

Same here.

The solution is to reformat the disk to ext4. After my feedback, the team at the Hostkey fixed the problem in a few hours. I like this type of service. Also, the provided server had only 1Tb of disk space, which is excellent for most problems, but not for this deep fakes challenge. I asked to increase the volume and it was also performed.

I did not participate in ML competitions for a couple of years and slightly out of shape. My most recent participation at Kaggle was not as a participant but as a [host](https://twitter.com/viglovikov/status/1235324143953903617).

Hence my results in deepfake are far from what it was when I was competing a lot, and my ML muscles were in much better shape.

Is the setup of the server optimal for Deep Learning? Optimal — no, pretty good — yes.

When you train networks, you should aim for 100% GPU utilization. It is an ideal situation. For my code at the local machine with fast CPU and fast SSD, GPU utilization is in the range of 80–95%. At the hostkey server, for the same code and the data, the number was a bit lower. The main reason is that 8xGPUs require faster disk and faster CPU for the preparation of the batch.

It was not a big deal, more like a message to the people that build their machines: "**GPUs are the key, but do not forget about the rest of the pipeline: CPU/disk or if you are streaming the data from S3 / GCP about the networking.**"

There is another small detail that I liked about the servers that Hostkey provided. When you train the network, the temperature of your GPUs goes up. When it becomes around 85 degrees celsius GPUs drop the frequency, which leads to a drop in performance. The drop is approximately 15%. There are different ways to avoid overheat and not lose performance. I do not know what Hostkey does for their cooling, but the temperature of the video cards was never above 60 degrees. It adds a bit of confidence about the stability of their solutions.

I loved the initiative by Hostkey, and I hope other companies will sponsor other competitors in future challenges.
