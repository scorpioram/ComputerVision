# ComputerVision
Face Mask segmentation
Here is the step by step guide on the Face Detection project.The complete project is divided into multiple sections:

Section 1 : 

Data Pre-Processing and reviewing the data:
    1. Mount Google drive 
    2. Change current directory to working directory
    3. Load the images from images.npy file. 
    4. Check sample of images data by plotting image using matplotlib.
    5. Set the dimension of the images to be trained and evaluvated.
    6. create images array and masks array by using the data loaded using the images.npy file.
       images.npy file contains 2 set of arrays for each images. One image array and second array has the image size and bounding box lists.
       Parse each bounding box and create the masks array for each images.
    7. print and check the images array and masks array shape are correct.
    8. Visualizing the images and masks.

Section 2:

    1. Unet with Decoder type = Upsampling: Create Unet Model using pre-trained Mobilnet as backbone network model and
       carefully create the decoder network model using upsampling and concatenate for skip connections additions.

    2. Unet with Decoder type = Transpose convolution: Create Unet Model using pre-trained Mobilnet as backbone network model and
       carefully create the decoder network model using Transposeconvlution and concatenate for skip connections additions.
    3. Define loss and metrics functions
    4. Define callbacks
    5. Compile both the models with Adam Optimizer and loss and metrics functions defined.
    6. Split the images into X_train, X_Valid and X_Test
       There are totally 409 images. We have split them into:¶
       X_Train = 399 images
       X_Validation = 5 images
       X_Test = 5 images
    7. Train both the models separately with 50 epoch and batch size=1
    8. Plot Learning curve[loss] and Accuracy[dice coefficient]



Section 3:

    1. Let's take 5 images from X_train and predict mask using both the models.
    2. Plot and Compare the images, Ground truth and predicted mask using both the models..
    3. Let's take 5 images from X_Valid and predict mask using both the models..
    4. Plot and Compare the images, Ground truth and predicted mask using both the models..
    5. Let's take 5 images from X_test and predict mask using both the models..
    6. Plot and Compare the images, Ground truth and predicted mask using both the models..

Section 4: 

    1. Let's use randomly downloaded images  from internet.
    2. Let's those images and predict mask using both the models..
    3. Plot and Compare the images, and predicted mask using both the models..

Saved model weights file is attached for evaluating.
