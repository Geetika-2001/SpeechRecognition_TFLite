
## EDGE ML TASK 3-Speech Recognition

This repository is contains a Speech recognition TF-Lite Model ,aimed at recognising Sound, Noise and Silence.It uses Tensorflow Lite to deploy a machine learning model in your smartphone. My machine learning model should be classifies between “Noise”, “Speech” and “Silence” audio signals.

## Documentation

[Documentation](https://linktodocumentation)

This colab notebook uses, TensorFlow Lite Model Maker to train a speech recognition model that can classify spoken words or short phrases using one-second sound samples. 
The Model Maker library uses transfer learning to retrain an existing TensorFlow model with a new dataset, which reduces the amount of sample data and time required for training.

It exports a TFLite model that you can run on a mobile device or embedded system (such as a Raspberry Pi). It also exports the trained model as a TensorFlow SavedModel.

## Prepare the dataset

To train with the default speech dataset, just run all the code below as-is.

## Generate a background noise dataset

Whether you're using the custom dataset, I have a good set of background noises so your model can distinguish speech from other noises (including silence).

Because the following background samples are provided in WAV files that are a minute long or longer, we need to split them up into smaller one-second samples so we can reserve some for our test dataset. We'll also combine a couple different sample sources to build a comprehensive set of background noises and silence:

## Prepare the speech commands dataset

This dataset includes over 30 speech command classifications, and most of them have over 2,000 samples. But because we're using transfer learning, we don't need that many samples. So the following code does a few things:

Specify which classifications we want to use, and delete the rest.
Keep only 150 samples of each class for training (to prove that transfer learning works well with smaller datasets and simply to reduce the training time).
Create a separate directory for a test dataset so we can easily run inference with them later.

## Load your dataset

Now you need to load your dataset according to the model specifications. Model Maker includes the DataLoader API, which will load your dataset from a folder and ensure it's in the expected format for the model spec.

## Train the model

Now we'll use the Model Maker create() function to create a model based on our model spec and training dataset, and begin training.

If you're using a custom dataset, you might want to change the batch size as appropriate for the number of samples in your train set.

## Review the model performance
Even if the accuracy/loss looks good from the training output above, it's important to also run the model using test data that the model has not seen yet, which is what the evaluate() method.

## Download the TF Lite model
Now you can deploy the TF Lite model to your mobile or embedded device. You don't need to download the labels file because you can instead retrieve the labels from .tflite file metadata, as shown in the previous inferencing example
## 🚀 About Me
I'm an ML enthusiast .I have previously worked on Computer Vision based projects and enjoy working with projects having realworld applications. I wish to contribute to tech!

  
## 🔗 Links
[![Medium](https://img.shields.io/badge/my_Medium-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://geetikakaushik2020.medium.com/)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/geetika-kaushik-a111681b8/)

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/GeetikaKaushik5)

  
