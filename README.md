# Building AI

Final project for the Building AI course project: UrbanNoise

## Summary

UrbanNoise is a mobile and web platform that uses AI to classify environmental sounds (e.g., traffic, construction, concerts) in real time and map urban noise pollution, offering insights and personalized alerts to city planners and residents.

## Background

Noise pollution impacts public health, urban quality of life, and environmental planning. Traditional monitoring relies on expensive equipment and sparse measurement points.

* Lack of real-time, high-resolution noise data  
* High costs of deploying and maintaining acoustic sensors  
* Limited citizen awareness about local noise exposure  

## How is it used?

Users open the UrbanNoise app on their smartphone to record audio snippets in their environment. The app extracts audio features (MFCCs) and uses a trained convolutional neural network to classify sound sources and estimate decibel levels. Data is sent to the web dashboard to update an interactive noise map.

In practice:
1. Open the app in any urban location.  
2. Record a 10-second audio sample.  
3. View real-time classification and noise level.  
4. Explore the web dashboard to see aggregated data and trends.  

![App screenshot](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*YO78LKnoSBN13qdpK84Uww.png)

Local image from GitHub repo:

![Noise map](/noise_map.png)

## Data sources and AI methods

We leverage the [UrbanSound8K dataset](https://urbansounddataset.weebly.com/) for initial model training and collect additional crowdsourced recordings via the mobile app. Audio samples are processed using the Librosa library.

| Method                    | Description                                              |
| ------------------------- | -------------------------------------------------------- |
| MFCC extraction           | Extract Mel-frequency cepstral coefficients from audio   |
| Convolutional Neural Network | Classify sound sources into predefined categories      |
| Regression layer          | Estimate sound pressure level (decibels)                |

## Challenges

UrbanNoise does not guarantee privacy-preserving recording: users must consent to audio capture. Model accuracy may degrade in extremely noisy or overlapping sound environments. Battery consumption and network connectivity can limit real-time data submission.

## What next?

To scale the project, we plan to:
1. Partner with local governments for sensor deployment.  
2. Incorporate edge-computing models to reduce data transmission.  
3. Expand sound categories (e.g., wildlife, construction machinery).  

We will need expertise in mobile development (iOS/Android), cloud infrastructure, and urban planning domain knowledge.

## Acknowledgments

* [UrbanSound8K dataset by Salamon et al.](https://urbansounddataset.weebly.com/) / CC BY SA 4.0  
* Building AI course template provided by Reaktor Innovations and University of Helsinki  
* Icons by [Freepik](https://www.freepik.com/) under CC BY 3.0  
