# Skin_disease_recognition
Built multiple neural network to recognise 8 different skin disease <br>
The project aims in recognising 8 differnt . 
## Dataset 
The dataset used here is the HAM10000 datset which contains 8 different skin diseases which are 
1)  Actinic keratoses and intraepithelial carcinoma / Bowen's disease (akiec)
2)  Basal cell carcinoma (bcc)
3)  Benign keratosis-like lesions (solar lentigines / seborrheic keratoses and lichen-planus like keratoses, bkl )
4)  Dermatofibroma (df)
5)  Melanoma (mel)
6)  Melanocytic nevi (nv)
7)  Vascular lesions (angiomas, angiokeratomas, pyogenic granulomas and hemorrhage, vasc)<br>
The dataset is in multiple forms where you get the dataset with images and a metacsv file , which contains columns as lesion_id,image_id	,dx	,dx_type,age,sex,	localization<br>
Also there is another form of the dataset which is as a csv which is represents every image compressed in the form of 28*28*3 pixel image , it contains 2353(28*28*3 + 1) columns which is 1 for every pixel plus the label of the image .
## Results
The results achieved with the different models were -
model - training accuracy - 61.92 %
      - validation accuracy - 56.68 %
model1 - training accuracy - 78.64 %
       - validation accuracy - 58.44%
model3 - training accuracy - 96.68 %
       - validation accuracy - 72.75 %
       - testing accuuracy - 70%<br>
model and model1 used the image dataset where oyt of of 10000 images only 1770 images were used for training and 794 imaged for testing to handle class imabalance , a better way to do thhis woould be making copies of the minority class and then training but as i was doing it on google colab making copies is a very  time consuming process so i decided too remove images from major class instead , if the full dataset is used accuracy can be increased significantly .<br>
In model 3 the 28*28*3 dataset is used so computation is less here , here we can make copies of the minority class easily fromm the dataframe , so oversampling is done to handle class imbalance and testing accuracy is 70 % , so even though only 28*28 pixel photos are used here we sstill get a 12 percent better accuracy than the case where we use iamges of size in the range of 400 * 400 pixel , so if we train the model on the better quality image data we wil get significantly better results.
