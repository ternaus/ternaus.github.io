---
layout: single
title:  "Multi-target in Albumentations"
excerpt: "Many images, many masks, bounding boxes, and key points. How to transform them in sync?"
categories: machine_learning
tags: albumentations tutorial

header:
    teaser: https://miro.medium.com/max/1750/1*lHMua9ruClZwHR8O0fyO7A.jpeg
    caption: Image source - https://www.newsbreak.com/news/1480496874024/elon-musk-revealed-his-favorite-film-of-2019-was-parasite
    og_image: https://miro.medium.com/max/1750/1*lHMua9ruClZwHR8O0fyO7A.jpeg
---
![](https://miro.medium.com/max/1750/1*lHMua9ruClZwHR8O0fyO7A.jpeg)

This article was originally posted at [Medium](https://towardsdatascience.com/multi-target-in-albumentations-16a777e9006e).

---
{% include toc title="Table of Contents" %}

I am one of the authors of the image augmentation library [Albumentations](https://albumentations.ai/).

Image augmentations is an interpretable regularization technique. You transform the existing data to generate a new one.

![](https://miro.medium.com/max/1750/1*Za3VLUEHu7JhiLRWO3Lv_A.jpeg)

*[](https://albumentations.ai/docs/introduction/image_augmentation)*

You can use the library with [PyTorch](https://www.kaggle.com/tarunpaparaju/alaska2-steganalysis-efficientnet-b3-pytorch), [Keras](https://github.com/qubvel/segmentation_models/blob/master/examples/multiclass%20segmentation%20(camvid).ipynb), [Tensorflow](https://colab.research.google.com/github/albumentations-team/albumentations_examples/blob/colab/tensorflow-example.ipynb), or any other framework that can treat an image as a numpy array.

Albumentations work the best with the standard tasks of classification, segmentation, object, and keypoint detection. But there are situations when your samples consist of a set of different objects.
Multi-target functionality specifically designed for this situation.

Possible use cases:
* Siamese networks
* Sequential frames in the video.
* Image2image.
* Multilabel segmentation.
* Instance segmentation.
* Panoptic segmentation.

## A few buzzwords
* The library emerged from the winning solutions in machine learning competitions. The core team includes one [Kaggle Grandmaster](https://www.kaggle.com/progression#grandmaster), three [Kaggle Masters](https://www.kaggle.com/progression#master), and one [Kaggle Expert](https://www.kaggle.com/progression#expert).
* [Selim Seferbekov](https://www.kaggle.com/selimsef), the winner of the $1,000,000 [Deepfake Challenge](https://www.kaggle.com/c/deepfake-detection-challenge), used albumentations in his solution.
* The library is part of the [PyTorch ecosystem](https://pytorch.org/ecosystem/) and the Nvidia Inception program.
* 5800+ stars at the [GitHub](https://github.com/albumentations-team/albumentations).
* [80+ citations](https://scholar.google.com/scholar?oi=bibs&hl=en&cites=13927538846757401282) in scientific papers. The library was mentioned in [three books](https://albumentations.ai/docs/external_resources/books/).

For the past three years, we worked on functionality and optimized for the performance.

Now we focus on [documentation](Now we focus on documentation and tutorials.) and [tutorials](https://albumentations.ai/docs/examples/).

At least once a week users ask to add support for multiple masks.

<a class="embedly-card" href="https://www.reddit.com/r/MachineLearning/comments/hu3i0z/d_we_need_your_questions_about_albumentations_the/fynf8ko">Card</a>
<script async src="//embed.redditmedia.com/widgets/platform.js" charset="UTF-8"></script>

We already have it for more than a year. :)

This article will share examples of how to work with multiple targets with albumentations.

## Scenario 1: One image, one mask

![](https://miro.medium.com/max/1750/1*lHMua9ruClZwHR8O0fyO7A.jpeg)

*The input image and mask.*

The most common use case is image segmentation. You have an image and a mask. You want to perform a spatial transform of both image and mask, and it should be the same set of transforms. Albumentations takes care of this requirement.

In the following code, we apply HorizontalFlip and ShiftScaleRotate.

<script src="https://gist.github.com/ternaus/a6a11847e3a1b0da41fc84de85476ef5.js"></script>

![](https://miro.medium.com/max/1750/1*5uLc6odMwOVO4OVyLUjigA.jpeg)

## Scenario 2: One image and several masks

![](https://miro.medium.com/max/1750/1*Yu7WQRLX_WAdNt2eYtOAig.jpeg)

*Input: one image, two masks*

For some tasks, you may have a few labels corresponding to the same pixel.

Let’s apply [HorizontalFlip](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.HorizontalFlip), [GridDistortion](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.GridDistortion), [RandomCrop](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.RandomCrop).

<script src="https://gist.github.com/ternaus/02f581143a9ebe4a89c1c690ab6736f9.js"></script>

![](https://miro.medium.com/max/1750/1*BRSE1p1DPJWpk4k5cJpXNA.jpeg)

## Scenario 3: several images, masks, key points, and bounding boxes

![](https://miro.medium.com/max/1750/1*bGTq__qLurb4schKMUzR9g.jpeg)

You may apply spatial transforms to multiple targets.

In this example, we have two images, two masks, two bounding boxes, and two sets of keypoints.

Let’s apply the sequence of [HorizontalFlip](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.HorizontalFlip) and [ShiftScaleRotate](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.HorizontalFlip)

<script src="https://gist.github.com/ternaus/5a4e47d640f0731850297ba84e4e351e.js"></script>

![](https://miro.medium.com/max/1750/1*-TeOkE5Lq0rHcq3dq3YgBQ.jpeg)

## FAQ

### Q: Can we work with more than two images?
A: You can use as many as you want.

### Q: Should the number of image, mask, bounding box, and keypoint targets be the same?

A: You can have N images, M masks, K key points, and B bounding boxes. N, M, K, and B could be different.

### Q: Are there situations where multi-target will break?

A: In general, you can use the multi-target functionality to a set of images of different sizes. Some transform depends on the inputs. For example, you cannot perform a crop that is larger than the image. Another example is MaskDropout that depends on the input mask may. How will it behave when we have a set of masks is unclear. We will test these corner cases. But they are pretty rare in practice.

### Q: How many transforms could be combined together?

A: You can combine the transforms into a complex pipeline in a number of ways.

We have more than [30 spatial transforms](https://albumentations.ai/docs/getting_started/transforms_and_targets/#spatial-level-transforms). All of them support images and masks, most of them support bounding boxes and key points.

![](https://miro.medium.com/max/1750/1*pvJuOaQDBUJeHBu3AIIyyA.png)

*[](https://albumentations.ai/docs/getting_started/transforms_and_targets/#spatial-level-transforms)*

That could be combined with [40+ transforms](https://albumentations.ai/docs/getting_started/transforms_and_targets/#pixel-level-transforms) that modify pixel values of the image. Example: [RandomBrightnessContrast](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.RandomBrightnessContrast), [Blur](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.Blur), or something more exotic like [RandomRain](https://albumentations.ai/docs/api_reference/augmentations/transforms/#albumentations.augmentations.transforms.RandomRain).

## More documentation

* [Full list of the transforms](https://albumentations.ai/docs/api_reference/augmentations/transforms/)
* [Mask augmentation for segmentation](https://albumentations.ai/docs/getting_started/mask_augmentation/)
* [Bounding boxes augmentation for object detection](https://albumentations.ai/docs/getting_started/bounding_boxes_augmentation/#bounding-boxes-augmentation-for-object-detection)
* [Keypoints augmentation](https://albumentations.ai/docs/examples/example_keypoints/)
* [Simultaneous augmentation of multiple targets: masks, bounding boxes, keypoints](https://albumentations.ai/docs/getting_started/simultaneous_augmentation/#simultaneous-augmentation-of-multiple-targets-masks-bounding-boxes-keypoints)
* [Setting probabilities for transforms in an augmentation pipeline](Setting probabilities for transforms in an augmentation pipeline)

## Conclusion

Working on the open-source project is challenging, but very exciting. I would like to thank the core team:
* [Alexander Buslaev](https://www.linkedin.com/in/al-buslaev/)
* [Vladimir Iglovikov](https://www.linkedin.com/in/iglovikov/)
* [Alex Parinov](https://www.linkedin.com/in/alex-parinov/)
* [Eugene Khvedchenia](https://www.linkedin.com/in/cvtalks/)
* [Mikhail Druzhinin](https://www.linkedin.com/in/mikhail-druzhinin-548229100/)

and all the [contributors](https://www.linkedin.com/in/mikhail-druzhinin-548229100/) that helped to build the [library](https://albumentations.ai/) and get it to its current state.
