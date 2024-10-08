# Image Caption Generation : A Hybrid Model Of Swin transformer and GRU attention
Image caption generation is the task of generating descriptive captions based on the content of images. In this project, images are first passed through the Swin Transformer layer for feature extraction. The extracted information is then fed into the GRU with attention to generate captions.

## Overview
This project aims to generate accurate captions by leveraging the strengths of both the Swin Transformer and GRU with attention. The Swin Transformer is used for its superior performance in feature extraction compared to other models. In the image captioning pipeline, the Swin Transformer serves as the encoder, while the GRU with attention acts as the decoder.

There are two key components in this image captioning model:

1. Swin Transformer
2. GRU with Attention Mechanism

Swin Transformer: 
The Swin Transformer is a hierarchical vision model that divides an input image into non-overlapping patches, processes these patches using transformers, and progressively merges them to create a multi-resolution representation. The key innovation of the Swin Transformer is the use of shifted windows, which balances efficiency and performance by reducing computational overhead while capturing both local and global image context. In this model, the Swin Transformer is responsible for extracting meaningful features from the image and passing them to the GRU attention layer for caption generation.

GRU Attention : 
GRU (Gated Recurrent Unit) is a type of recurrent neural network (RNN) used for handling sequential data like text. In image captioning, the GRU generates the caption word by word. It works as the sequence generator, predicting the next word in the caption based on the image features from the encoder and the previously generated word. The attention mechanism allows the model to focus on relevant parts of the image for each word, ensuring context-aware caption generation.

This combination of the Swin Transformer and GRU with attention allows the model to focus on specific parts of the image during the caption generation process, leading to more accurate and contextually relevant captions.

## Dataset 
The dataset used in this project is the Flickr30k dataset, which contains 30,000 images with corresponding captions. Each image is paired with five different captions, providing diverse descriptions that help train the model more effectively. The dataset is sourced from the Hugging Face website.
[Dataset](https://huggingface.co/datasets/nlphuji/flickr30k/tree/main).

## Conclusion
The model should be trained for more epochs to improve accuracy. I trained the model for 80 epochs, which yielded results, but they were not sufficiently accurate. A high-performance GPU is required to train this model effectively and achieve better results.