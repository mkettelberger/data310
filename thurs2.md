1. For the beans dataset, I tried different numbers of epochs to attain better accuracies.
With only three epochs, the accuracy was around 0.7231 with loss around 0.6593.
   When I increased the epochs to 10, the accuracy reached 0.9734 with a loss of 0.0971.
   There is a possibility that the model could be slightly overfit at this point because the validation
   accuracy was 0.7404 which is much lower, but still reasonable.
   I hesitated to increase the epochs anymore because already the three and ten where taking a large chunk of time.
   While I'm not sure the precise time ten epochs took, I know three took about 4 or 5 minutes. An interesting part of the data happened at just three
   epochs where the validation accuracy was 0.7885, which was higher than the regular accuracy of 0.7231. This is probably just a random result, and should be
   addressed by simply running the model a few more times and averaging the results.
   
    I predict this model was more accurate than the eurosat model at the higher number of epochs because
    this dataset only had three different possible labels while eurosat had ten. Also, the bean images were much
   larger (500x500) than the eurosat images (64x64). However, this could possibly allow for more error, but it could also mean that there are
   more details on the larger pictures to distinguish them better.
   

2. For the eurosat dataset, I also managed to increase the epochs to increase accuracy. First at three epochs, the accuracy was 0.7475 and 
loss was 0.7136. Since this model was a little faster than beans, I increased the epoch number to 20. It resulted in an accuacy of
   0.9349 which was lower than I had hoped it would be given how ten epochs for the beans increased it so much.
   

3. After applying augmentation to the tf_flowers dataset, I received the following results after three epochs: loss: 1.0127 - accuracy: 0.6015 - val_loss: 1.0499 - val_accuracy: 0.5967.
I was able to increase the epochs to 10 and got the following results: loss: 0.7738 - accuracy: 0.7030 - val_loss: 0.8360 - val_accuracy: 0.668.
   The model was able to better predict, but this could be due mainly to the fact that the number of epochs increased. Without having the augmentation in the code and still doing ten epochs, the accuracy increased to 
   0.9724 which is about 0.27 better than the augmented version.
   


4. Using augmentation on the beans data set, the highest accuracy I got was 0.8525 (ten epochs). This is to be compared with the 0.9734 accuracy (ten epochs) and 0.7231 accuracy (three epochs). As one can see, in these cases, augmentation
did not increase the success of the model. However, the accuracy was higher than the regular dataset with three epochs but that's mainly due to the increase in epochs. For the eurosat data, augmentation yielded results with a 0.5215 accuracy (twenty epochs). This can be compared to the 0.9349 accuracy (twenty epochs) and 0.7475 accuracy (three epochs). Similar to the beans dataset, augmentation did not help 
the model get more accurate predictions. In fact, it made it significantly worse.
   
With both datasets after augmentation, I noticed that fitting the model took much less time most likely because the images were smaller and easier to iterate over.





