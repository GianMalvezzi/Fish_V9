# Fish Classification

In this project a fish classification model was trained using a public [Kaggle dataset](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset). The strategy of freezing some of the layers of the pre-trained model was used to speed up its training, Since the InceptionV9 model has more than a million parameters. We can exemplify this with a flowchart from the article [Train Deep Learning Network to Classify New Images](https://la.mathworks.com/help/deeplearning/ug/train-deep-learning-network-to-classify-new-images.html):

![](https://la.mathworks.com/help/examples/nnet/win64/TransferLearningUsingGoogLeNetExample_01.png)
