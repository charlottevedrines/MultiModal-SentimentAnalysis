# MultiModal-SentimentAnalysis

This project was developed by three third year engineering students from the University of Toronto as part of their coursework for APS360: Applied Fundamentals of Deep Learning.

## Interpreting User Sentiment in Instagram Posts: A Multimodal Deep Learning Approach

In the age of social media, Instagram serves as a prominent platform for users to express themselves through visual and textual content. However, deciphering the sentiments behind these posts, often laden with irony and cultural nuances, poses a significant challenge due to the intricate interplay between images and text. Being able to accurately classify the sentiment of an Instagram post would provide valuable insights for businesses seeking to gauge customer reception of their brand, or for sensitive users who wish to filter out negative posts from their feed. 

This repository introduces a multimodal deep learning approach aimed at interpreting user sentiment in Instagram posts by analyzing both visual and textual elements. Our proposed model integrates two parallel deep learning networks that process images along with their associated caption and comments. The conclusion of the post’s overall sentiment would be deduced from a trainable weighted average of the two model predictions. We aim to develop a robust sentiment analysis model that can draw information from both the image post and associated caption to enhance user experience and engagement on Instagram across both commercial and personal spheres.

![image](https://github.com/charlottevedrines/MultiModal-SentimentAnalysis/assets/97196465/e49b547e-7c5b-44a5-8429-6a562d9bb9cd)

The diagram visualizes the pipeline of the architecture, featuring a dual deep learning model that processes two inputs from Instagram posts: an image and its caption, through two distinct models. The sentiment class of the post is determined by a trainable weighted average, acting as an attention mechanism.

The [full report](Final_Report.pdf) written by all three collaborators is publicly available.

## Running the model

This model can be ran on CPU or GPU. The image and text model have been pretained by our team and downloaded [here](https://drive.google.com/drive/folders/1zHkLyKiJEYuhGtAWvzRjDNOG05ZUNJav?usp=drive_link). Due to the lack of open source dataset Instagram posts (including image and text) labelled with their sentiment, our team collected our own test set totalling to 240 labelled images with their corresponding captions. This custom test set

A google colab has been uploaded in this repository and contains the code that uploads the pretrained models, passes them our test dataset, records the results of both models in a pandas dataframe before passing the results to the weighted average neural netowork that performs a holistic evaluation on the entire Instagram post.
