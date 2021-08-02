1. The model gave us shorter lines, and we added our own character names. The script didn't need
too much modification, so we used the customized script. After 500 epochs, the final loss was around 0.0316, and the initial loss
   was 4.35. 
   
2. Our text output was more short term and seemed very conversational. The model seemed to notice that it was 
different characters speaking even though we hard coded the names in. For some of our models,
   we copied the script multiple times to give the model more data to work with.
   
3. We ended up using the customized training model which was able to use curriculum learning using train_step to
learn from past mistakes starting with easier data and getting harder. It uses a tf.gradient to apply updates and rerun the model in a loop.

4. There were many repeated phrases specific to each character such as Barry saying "free the bees." The model seemed to 
actually figure out what each individual character was most likely to say, and it was able to repeat that. The lines fit together 
   surprisingly well as a back and forth dialogue. The output also had multiple lines where it was able to name specific names from the movie, including 
   the airport.


![Flowers](Images/flowers.png)