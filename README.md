## Problem Statement

The problem is to design and implement a model to automatically generate textual description for given images. Nowadays, problems such as image classification and natural language processing have been well studied. However, linking the two fields is quite tricky. This model is expected to recognize the objects in the image and find the relationship between them. Additionally, the model should be able to use a language such as English to represent the relationship. Recognizing images has already been applied to many fields such as medical research, self-driving cars, and facial recognition. Besides, solving this problem can create high business value. For example, helping visually impaired people better understand the content of images on the web [1].

## Data Set
In this project, we are using Common Objects in Context (COCO) dataset [2]. This dataset contains a large volume of images that represent common objects in our everyday scenes. It is widely used by academia for object detection, image segmentation, caption generation, and so on. The author of the paper claims that the dataset contains 91 types of objects that would be easily recognized by 4-year-old kids. The image captions are stored in Image Caption Annotations. Each caption describes the corresponding image. Each image has at least five captions.

## Project Idea

First, we will use transfer learning such as VGG16 and RESNET to perform as an ‘encoder’ to preprocess the images and generate vector representation that could be used by a ‘decoder’ that generates the caption. Then, to address the problem of the computational complexity of RNN, we will use Attention Model to extract important features. Finally, we use RNN such as bi-directional LSTM, GRU as a decoder to generate a sentence to describe the image.

It is convenient to evaluate our models by simply submitting the results to Microsoft COCO Captions: Data Collection and Evaluation Server. It remains open after the competition was over in 2015.

## Papers to Read

Based on our search, the image captioning problem is discussed extensively in the academic world. Most proposed solutions take the idea of machine translation and employ a CNN encoder and RNN decoder in their implementations. We have read two recent papers on image captioning. The first one is written by Google and talks about the “show and tell” model [3]. They build a model consisting of a vision CNN and a language generating RNN and evaluate it on datasets such as Flickr30k and MSCOCO. The BLEU score of this model is higher than the current state-of-art model. Another paper is based on the “show and tell” model and incorporates “attention” into the model [4]. This approach further improves the BLEU measure on Flickr and MSCOCO datasets. We also plan to read more papers on CNN, RNN, and their application on translation machine and image captioning to gain insights about improving the current models.

## Final Goal and Planned Schedule

Our final goal would be to build an image captioning model that achieves high BLEU score on Flickr and MSCOCO datasets. We will follow the detailed timeline of the project strictly. We plan to implement the pre-existing algorithms and come up with new ideas to improve the algorithms.

## References

[1] Vinyals, O., Toshev, A., Bengio, S.& Erhan, D. (2015) Show and tell: A neural image caption generator. 2015 IEEE Conference on Computer Vision and Pattern Recognition (CVPR). doi:10.1109/cvpr.2015.7298935

[2] Tsung-Yi Lin, Michael Maire, Serge Belongie, James Hays, Pietro Perona, Deva Ramanan, Piotr Dollár & C. Lawrence Zitnick (2014) Microsoft COCO: Common Objects in Context Computer Vision – ECCV 2014 Lecture Notes in Computer Science pp. 740--755. Springer, Cham
  
[3] K.Xu, J.Ba, R.Kiros, A. Courville, R. Salakhutdinov, R. Zemel & Y. Bengio (2015) Show, attend and tell: Neural image caption generation with visual attention. 2015 IEEE Conference on Computer Vision and Pattern Recognition (CVPR). arXiv preprint arXiv:1502.03044, 2015.
