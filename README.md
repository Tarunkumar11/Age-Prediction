# Age-Prediction
Age prediction  unsing convolution Neural Network

Dataset
The Dataset I have use is the UTKFace.UTKFace dataset is a large-scale face dataset with long age span (range from 0 to 116 years old).
The dataset consists of over 20,000 face images with annotations of age, gender, and ethnicity. The images cover large variation in pose,
facial expression, illumination, occlusion, resolution, etc. This dataset could be used on a variety of tasks, e.g., face detection, age 
estimation,age progression/regression etc

How I classify the dataset:
Because i was going to use this model for mobile appliction for childrens.So the main focus of me to predict the age 1-18 with great acuuracy.
so from 100+ classes of dataset i combined the classes and make them 6 clsess. Before this i classify them between male and female.So the 
final look of the dataset was like that:
train:
     male:
        (1-5)
        (6-10)
        (11-15)
        (15 -17)
        20+
    Female:
        (1-5)
        (6-10)
        (11-15)
        (15 -17)
        20+
This was the same for testing dataset too.

Designing the of Model:
To design the Deep Learning model I used the Transfer Learning. Here I used a pretrained model Mobile Net which is widely use for mobile applications.
It's output layer contains 1000 classes for I remove this last layer and freeze of it's starting 60% layer add some layer at end to get the
predictes value.

Traing of the Model:
I trained the designed model on the UTKFace dataset.For this optimization 'sgd' function is and used and error is calculted by the 'sequre mean error' function.

Prediction of model:
To predict the age from a Image I applied some preprocessing on it. and I  used openCV for that
First to check whethere the Image contain fase or not.This is done by opencv inbuild library "haarcascade_frontalface_alt.xml".
so if there is an face in Imge it crop the face. and croped Image is used to predict the age.

    
        
        
