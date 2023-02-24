# Mini-Project-3---Scene-Recognition
# Introduction
    In this project , we are building a scene recognition model.Scene recognition is one of
    the classical computer vision problems in which the model tries to classify images of
    different scenes.
    Using three different approaches to solve this problem which are :
    1. Tiny image with KNN classifier.
    2. Bag of words with KNN classifier.
    3. Bag of words with one vs.all linear SVM.
    
# Results

      ● After tuning parameters that's what we got :
      1) Pixel per cell =8 ,cells per block =2
      2) K Means with following parameters :
      MiniBatchKMeans(n_clusters=vocab_size, random_state=0,
      max_iter=300,batch_size=1500).fit(All_features).cluster_centers_
      3) Linear SVC with c=1.0 (a lot of regularization values between .1
      :5000 )
      4) K=1 is the best one worked for us after trying k=1,2,3
      5) Vocab size =200 best one out of 8 different sizes as below
      
# Performance  
    1.Tiny images with knn 
      Accuracy :23.867%
      Comment : that is no surprising as we lost most of the information when resizing each image to small size 
    
![confusion_matrix](https://user-images.githubusercontent.com/49596777/221071533-c8d8a974-88b3-4a86-929a-4cbf49d1fe37.png)

    2.Bag of words with 1nn
      Accuracy :  53.733%
      Comment : Much better than tiny image which not surprising as with bag of words we now have more sophisticated and representative representation 



    3.Bag of words with Multiclass LinearSVM 
       Accuracy :66.867% ~67%
       Comment : Linear svm gives best accuracy between them all as stated with the reason behind this in the project file description 
       ![confusion_matrix](https://user-images.githubusercontent.com/49596777/221071709-b0879d6a-ff27-4a02-a84c-cb530e0338cf.png)

![confusion_matrix](https://user-images.githubusercontent.com/49596777/221071790-8975cda4-a3c8-47e1-bcf6-74a36a3bf8f7.png)
