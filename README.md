# Transfer-Learning-and-Object-Localization

1. Create a labelled image classification dataset, OR choose an existing one. It should include exactly 2
classes. The classification problem should be suitable for deep convolutional networks, e.g. not trivially
solved with colour thresholding. If you like, you can choose just two classes from an existing dataset. If
using an existing dataset, do not use MNIST, Fashion MNIST, CIFAR, ImageNet, or any subset of
them. Update: do not use a dataset created for any previous module, such as the SUV versus Sedan
car dataset. Write a short paragraph to describe the dataset: background, size/shape, classes, method
of collection. Include a typical image from each class.

2. Choose any pretrained image classification model, e.g. one of those found at https://keras.io/api/a
pplications/. Import it, excluding the dense classification head. Make sure to use the appropriate
preprocessing for input images. We will call this the base model. Add layers to the base model and
train them to produce classifications on your dataset. Report your choice of base model; state and
explain the shape of the base model’s output; explain the layers you added and training carried out;
report classification performance on unseen data.

3. Now investigate the base model as follows. Extract a scalar output from each neuron in the final layer
of the base model. You can use a GlobalMaxPooling2D layer or GlobalAveragePooling2D, or another
method if you prefer. Add a Softmax layer after. Using this, identify one or more neurons whose
scalar output is strongly correlated with the class label of your dataset. Such neurons can
be seen as (weak) class detectors. Specify your method, state results, and give brief interpretation of
the results.

4. Now build a simple approach to object localisation, that is deciding where in the input image an object
is present, as follows. For each neuron identified in (3), write code to visualise its 2D output. Use
this to write a brief comment: does this 2D output allow localisation of objects in the input
image? Include several example images and the corresponding 2D outputs to support your comment.
Note: if we fail to make step (3) work, step (4) can still be attempted by choosing some neurons
manually. By the way, this approach is related to but not very similar to state of the art systems for
object localisation, such as YOLO. We are not required to investigate such systems in this assignment.
