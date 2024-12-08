#  Predicting Sale Price of a Listing

_Authors: Nathan Robertson, Mijee Kim, Josh Iwanicki_

## Introduction

_This repository represents the capstone project for the authors in the Masters of Applied Data Science (MADS) program at the University of Michigan. This is a home price prediction project leveraging machine learning, generative AI, and computer vision._

Determining what price you should sell your home for can feel like more of an art than a science. While major home marketplace websites like Zillow provide machine learning-based estimates of a home’s value (“Zestimate”), it does little to educate home buyers and sellers on the nuances that drive home price. In the research community, many research projects focus on data about the listing found online. These lead to explainable models, but they miss many of the variables a more sophisticated model like Zestimate incorporates.

We hypothesize that enriching listing data with points of interest (POI) data reflecting the surrounding environment and labeled images of the homes can significantly increase price prediction accuracy. By incorporating image classification, we aim to capture qualitative features such as the condition and aesthetic appeal of the home, which are often overlooked in models. Moreover, POI data offers insights into neighborhood context, such as proximity to schools, parks, and other features that can impact home values.

In this report, we outline the existing literature, present the methodology behind our approach, and deliver an evaluation of our results. We seek to communicate how blending multiple data sources, as well as blending tools across machine learning, computer vision, and generative AI delivers an open source, interpretable model of home pricing that provides valuable insights for both buyers and sellers in the real estate market.

[The full report can be found here](https://docs.google.com/document/d/1bIc3J4sXRWWcBvTOaUCBsZWUrenWeIn1PhI0KEX_0r4/edit)

## Getting Started

Clone the repo.

```
git clone https://github.com/n-c-robertson/MADS-capstone.git
```

Get all of the dependencies needed.

```
pip install -r requirements.txt
```

To run all of the code in this project, you will need API keys to a few different resources.

| API | Documentation to set up API key |
| ------------- | ------------- |
| Microsoft Azure Vision | [Link (Requires Credit Card)](https://learn.microsoft.com/en-us/answers/questions/126140/service-url-and-api-key-of-computer-vision) |
| OpenAI | [Link (Requires Credit Card)](https://platform.openai.com/docs/quickstart) |
| FBI Crime Data | [Link (Free)](https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi) |

## Accessing the Data

The data used for this project can be found in the team's Dropbox [Link](https://www.dropbox.com/home/Nathan%20Robertson/MADS-Fall-2024-Zillow-Predictive-Pricing). If you need access, please request access from natorobertson@gmail.com.

Download all of the data in Dropbox, and put it in the same directory as the notebook you are trying to run. Assuming you have the necessary API keys (documented above), you should be able to run the notebook.
