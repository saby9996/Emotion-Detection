# **Pet Emotion Detection**
 
 [SCIe Publication](https://www.mdpi.com/2076-3417/9/22/4938)

![Flow of Project](https://i.ibb.co/xLwJ2Jr/flow.png)


For emotion detection, the data from 10 different dogs were fetched of varied sizes, breeds, and age. The data that was fetched from the dogs were typically from 3 different movements namely, Right, Left and Straight Wag which determines Positive, Negative and Neutral emotion respectively. The data extraction process leveraged a camera for determining frames of the recorded video for identifying the “Emotion” ground truth of the dogs. Moreover, with regard to the sensors. One wearable device was attached to the dog and that is on the tail. The wearable sensor that was used for the process sampled Accelerometer and Gyroscope data. The fetched data was quite mammoth in size because the sensors sampled the data at a frequency of 33.3 Hz. The total size of the data that was fetched had 49,926 samples from all the 3 emotions.

![enter image description here](https://i.ibb.co/58kR6s5/emotion.png)

The data that was received consisted of a huge amount of noise as the signals were generated from the pets, therefore, some instances of disturbance in data fetch is unavoidable. Therefore, to reduce the amount of noise a “Lowpass Butterworth” filter was used. The Butterworth filter of the 6th order was used with the cutoff frequency of 3.667 Hz. The order of the filter was chosen on the basis of blocking the maximum noise and the cutoff frequency was decided on the basis of exploratory data analysis.

Post filtering and noise removal of the data, a routine of feature engineering was performed to fetch out important features from the data. For feature engineering 10 features for each axis of the accelerometer and gyroscope of the tail wearable device were derived using statistical methods and also domain knowledge. The features derived were, Mean, Standard Deviation, Mean Absolute Deviation, Minimum, Maximum, Energy Measure, Inter Quartile Range, Skewness and Kurtosis. All the features were calculated on the basis of a Rolling Window for 66 Samples with a Step Distance of 32 Samples which means every window must have different values in terms of the features which determine the optimum variance in the features. The number of features that were generated post feature engineering was 72 for all the axis for the tail wearable device. By using these features, we have also trained our model with various machine algorithms such as Random Forest, SVM, KNN, Naïve Bayes, and ANN. Finally, Performance comparison of different machine learning algorithm has been performed.
## Web Application 
![enter image description here](https://i.ibb.co/tbZSvBt/emotion-app.png)