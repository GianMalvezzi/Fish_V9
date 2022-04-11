# Fish Classification

In this project a fish classification model was trained using a public [Kaggle dataset](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset). The strategy of freezing some of the layers of the pre-trained model was used to speed up its training, Since the InceptionV9 model has more than a million parameters. We can exemplify this with a flowchart from the article [Accelerating Deep Learning Inference via Freezing](https://www.usenix.org/system/files/hotcloud19-paper-kumar.pdf):

![enter image description here](data:image/png;base64,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)

