# Arthropod-Object-Detection

Arthropods such as Spiders, Beetles, Flies are very difficult to observe and capture. As such building a model that could be used to automate identifying and capturing Arthropods could be very useful.

The Kaggle Notebook can be viewed [here](https://www.kaggle.com/code/rishabh222/arthropod-object-detection)

## Data

The data has been taken from Arthropod Taxonomy Orders Object Detection Dataset which is a dedicated dataset for Arthropods. The link for the dataset can be found [here](https://www.kaggle.com/datasets/mistag/arthropod-taxonomy-orders-object-detection-dataset). A sample image from the dataset is also shown below.

![Sample image from dataset](https://github.com/Risdorn/Arthropod-Object-Detection/assets/75654063/81416ebb-bcf2-4b8a-a70a-c3b1a9cdd8b6)

## Dataset

Along with the image, the dataset also contains json file with data regarding the bounding box. A sample image is shown below.

![Sample Image with Bounding Box](https://github.com/Risdorn/Arthropod-Object-Detection/assets/75654063/490a9ae2-6f41-4dff-aa2d-76189ebbc1fe)

We have 2 tasks, first is classifying the images into their respective labels and second is regression to find the location of bounding box. Bounding box location is found by 4 variables, coordinates of top left corner, the length and height of the box.

## CNN Architecture

The CNN Architecture contains 3 Convolution and Average Pooling layers followed by a Dense layer. Then it seprates into two different outputs, one for classification and other for regression.

![CNN Architecture](https://github.com/Risdorn/Arthropod-Object-Detection/assets/75654063/2ccc0dae-ec2f-4ad0-9db2-5cb3da97e3dd)

## Output

![Test Data Results](https://github.com/Risdorn/Arthropod-Object-Detection/assets/75654063/3ecdfb7c-c0a8-4010-ac12-09c6c4d7c4c0)

A few test data results are shown above. Green Boxes translate to correct classifications and Red Boxes represent misclassifications. IOU score represents the overlap between the correct bounding box and the predicted bounding box.

## References

https://medium.com/mlearning-ai/building-your-own-object-detector-from-scratch-with-tensorflow-bfeadfaddad8

https://github.com/doleron/simple-object-detector-from-scratch/blob/main/simple_obj_detector.ipynb

