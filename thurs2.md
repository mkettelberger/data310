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