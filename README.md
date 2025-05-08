# Kaggle AI vs Human Generated Image Classification
As part of the [Kaggle 2025 Women in AI (WAI) Challenge](https://www.kaggle.com/competitions/detect-ai-vs-human-generated-images)

[Dataset Link](https://www.kaggle.com/competitions/detect-ai-vs-human-generated-images/data)

The challenge was to classify AI from human-generated images, scored by macro F1 and test on the out-of-distribution test set containing images from unknown sources and generators while training set only contained Shutterstock and DeepMedia images.
 
Our final model was a soft voting ensemble that aggregates the prediction probabilities from diverse model types (foundational, spatial, frequency-based) with fine-tuned hyperparameters and an optimized decision threshold.

- Attained a 73% final F1-score.
- Applied content-aware data splitting using BLIP captioning and K-means clustering. 
- Researched and investigated artifacts using foundational (RegNet, ConvNeXt), spatial (CLIP ViT), frequency (DCT, FFT, noise residuals), photo forensics and non-deep learning solutions (Autogluon AutoML).
- Proactively benchmarked model on an open-sourced 1-million dataset ([GenImage](https://neurips.cc/media/neurips-2023/Slides/73644.pdf)) to identify performance gaps across generators like ADM, BigGAN, GLIDE, MidJourney, Stable Diffusion v1.4 & 1.5, VQDM, Wukong.

Feel free to check out the implementations and the thought processes behind them! 💡
