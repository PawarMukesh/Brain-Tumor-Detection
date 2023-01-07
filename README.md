# Brain-Tumor-Detection

# BUSINESS CASE: BASED ON BRAIN MRI IMAGES DATASET WE NEED PREDICT BRAIN TUMOUR

# TASK: BINARY CLASSIFICATION

![image](https://user-images.githubusercontent.com/101791322/211158791-5a7192c2-78c1-40dc-a73f-8e0e955645fa.png)

## DATA SUMMARY
**Total 274 Jpg Images are present In two classes**
- No ----> 119
- Yes ----> 155


## DEVICE THE PROJECT INTO MULTIPLE STEPS
- Prepare training, validation and testing set
- Get all classes labels
- Visualise training images
- Used CNN & VGG19 model
- Model Compilation
- Model Training
- Model Evaluation
- Model Saving
- Prediction on test data

## Architecture of prepare CNN model

![image](https://user-images.githubusercontent.com/101791322/211158933-250dbc14-3663-4d2a-a7f4-9bc1fb405020.png)


## Compile & Train Model
* Use binary crossentropy loss with adam optimizer and metrics is accuracy
* Balance the class weights
* Train model of 80 epoch and use model checkpoint to save the best model
* Plotting training, validation loss as well as accuracy

![image](https://user-images.githubusercontent.com/101791322/211159015-5384a333-3d52-40a9-9b8f-30f39de8a0a7.png)

![image](https://user-images.githubusercontent.com/101791322/211159542-2476910a-1d86-4364-9a86-2dc448b0ecbc.png)


**Achieved 88.24% testing accuracy**



## Used VGG19 transfer learning technique to get better accuracy

- Import vgg19 library and set input image size & used imagnet dataset weight as well as not include fully connected layer at top
- Freeze the existing weights
- Add more layers with sigmoid activation function

## Architecture of VGG19 model

![image](https://user-images.githubusercontent.com/101791322/211159374-bd5f5fb7-b10a-45d6-af46-5383a6c86872.png)


## Compile & Train model

* Use binary crossentropy loss with adam optimizer and metrics is accuracy
* Train model of 60 epoch and set the class weight
* Plotting training, validation loss as well as accuracy

![image](https://user-images.githubusercontent.com/101791322/211159525-175a952d-87b2-44ac-a21a-ff7d0ae21282.png)

![image](https://user-images.githubusercontent.com/101791322/211159443-7d0059d2-032c-4b61-b3c7-5b47061af787.png)

### Save model

**Achieved 92.16% testing accuracy**


