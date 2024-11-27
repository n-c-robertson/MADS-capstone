#  Predicting Sale Price of a Listing

_Authors: Nathan Robertson, Mijee Kim, Josh Iwanicki_

## Introduction

_This repository represents the capstone project for the authors in the Masters of Applied Data Science (MADS) program at the University of Michigan. This is a home price prediction project leveraging machine learning, generative AI, and computer vision._

Determining what price you should sell your home for can feel like more of an art than a science. While major home marketplace websites like Zillow provide machine learning-based estimates of a home’s value (“Zestimate”), it does little to educate home buyers and sellers on the nuances that drive home price. In the research community, many research projects focus on data about the listing found online. These lead to explainable models, but they miss many of the variables a more sophisticated model like Zestimate incorporates.

We hypothesize that enriching listing data with points of interest (POI) data reflecting the surrounding environment and labeled images of the homes can significantly increase price prediction accuracy. By incorporating image classification, we aim to capture qualitative features such as the condition and aesthetic appeal of the home, which are often overlooked in models. Moreover, POI data offers insights into neighborhood context, such as proximity to schools, parks, and other features that can impact home values.

In this report, we outline the existing literature, present the methodology behind our approach, and deliver an evaluation of our results. We seek to communicate how blending multiple data sources, as well as blending tools across machine learning, computer vision, and generative AI delivers an open source, interpretable model of home pricing that provides valuable insights for both buyers and sellers in the real estate market.

[The full report can be found here](https://docs.google.com/document/d/1bIc3J4sXRWWcBvTOaUCBsZWUrenWeIn1PhI0KEX_0r4/edit)

## Key Visuals

**Computer Vison Model Performance**

Our first layer of the model, predicting the class of a Zillow listing image (class=Bathroom, Bedroom, Kithcen, Living Room, Location Exterior, Other) performed with a weighted average F1 score of 0.79. Our second layer of the model, predicting the quality of a listing image (quality=1 to 10 score, with a different model for each class) performed with a mean absolute error of 1.24 - 1.30 across the different image classes.

| Image Classification (All Classes)  | Image Rank (Class=Bathroom) |
| ------------- | ------------- |
| ![Figure 1](https://drive.usercontent.google.com/download?id=1pp3Olo2gGwF1DVFQDUIuK6dXcGug7MA1)  | ![Figure 2](https://drive.usercontent.google.com/download?id=1PATYQzxk-h-PhI7pCc9deF4VVc9B3Tf2)  |

**Pricing Model Performance**

`WRITE WORDS HERE ONCE MODEL IS FINALIZED, AND UPDATE IMAGES.`

| Prediction  | MAE vs MAPE by Price |
| ------------- | ------------- |
| ![Figure 1](https://drive.usercontent.google.com/download?id=1Hlpk2bEV_xh0M-WxtxF9X1PmITMKttih)  | ![Figure 2](https://drive.usercontent.google.com/download?id=1i26B5PaqtpRDnfCikV182llPqcpbzRAZ) |

| Errors Heatmap (Count)  | Errors Heatmap (%) |
| ------------- | ------------- |
| ![Figure 1](https://drive.usercontent.google.com/download?id=1If4gWJpHYOTb1sJbyZrMgK85NV-R3xuX)  | ![Figure 2](https://drive.usercontent.google.com/download?id=1ytpbzP-dvaskXw5Z-q06Ry4QjLDcpAem)  |

## Accessing the Data

The data used for this project can be found in the team's Dropbox [Link](https://www.dropbox.com/home/Nathan%20Robertson/MADS-Fall-2024-Zillow-Predictive-Pricing). If you need access, please request access from natorobertson@gmail.com.

## Resources**

* Dropbox link to data: [Link](https://www.dropbox.com/home/Nathan%20Robertson/MADS-Fall-2024-Zillow-Predictive-Pricing) (Only availble to project members)
* Report link: [Link](https://docs.google.com/document/d/1bIc3J4sXRWWcBvTOaUCBsZWUrenWeIn1PhI0KEX_0r4/edit)
* Miro board link: [Link](https://miro.com/app/board/uXjVLWxCxnA=/)
* Trello board link: [Link](https://trello.com/b/e0sR9M4E/project-zillow-mads-capstone)
