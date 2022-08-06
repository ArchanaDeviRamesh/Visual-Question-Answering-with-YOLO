# Visual-Question-Answering-with-YOLO
Implementing Hierarchical Question-Image Co-Attention for Visual Question Answering with YOLO and Back Translation

* This work extends two enhancements to the existing Hierarchical Question-Image Co-Attention for Visual Question Answering [1]

# Problem Definition

  1) Image features extracted using CNN pre-trained on ImageNet(Xception) and with object features extracted from the YOLOV4 model pre-trained on MS COCO inspired by [2]
  2) Expanding the training dataset using Back Translation text data augmentation method (implemented only on the x_train data). 
 
 # Dataset used : VQA V2 (https://visualqa.org/download.html)
    1) In V2, train and validation dataset used with Split 1 means the training dataset will be used for both training and validation and the validation dataset will be used for testing (https://github.com/GT-Vision-Lab/VQA_LSTM_CNN)
 
 # Repository folders
 
 * "code" folder contains the code base for this work
    1) TrainSet.ipynb is used to create the train.csv file (training dataset). The same can be used to create val.csv (testing dataset). 
    2) VQA_Attention_Hierarchical_YOLO.ipynb contains the implementation of Hierarchical Question-Image Co-Attention with YOLO
    3) VQA_Attention_Hierarchical_YOLO_BT.ipynb contains the implementation of Hierarchical Question-Image Co-Attention with YOLO and Back Translation
    4) BackTranslation.ipynb contains the implementation of Back Translation creating x_train_da.csv and y_train_da.csv
    
 * "data" folder contains the csv files used for implementation.
    1) train.csv 
    2) val.csv
    3) x_train.csv, y_train.csv, x_test.csv and y_test.csv used in VQA_Attention_Hierarchical_YOLO.ipynb
    4) x_train_da.csv, y_train_da.csv, x_test.csv and y_test.csv used in VQA_Attention_Hierarchical_YOLO_BT
    (X and Y train and test csv files are created using train_test_split API internally)  
 
 # References: 
 
 [1] Lu, Jiasen, Jianwei Yang, Dhruv Batra, and Devi Parikh. ”Hierarchical question-image co-attention for visual question answering.” Advances in neural information processing systems 29 (2016)
 
 [2] Al-Malla, Muhammad Abdelhadie, Assef Jafar, and Nada Ghneim. ”Image captioning model using attention and object features to mimic human image understanding.” Journal of Big Data 9, no. 1 (2022): 1-16.
