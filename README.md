# Classifying images as memorable or not with a random forest classifier

CNN and GIST features were collected on pictures that were hand-labelled as memorable or not. We implemented a Random Forest Classifier (RFC) to predict their label. We experimented with the hyper-parameters of the RFC and with feature pre-processing techniques, but found they had no positive effect on our model’s accuracy. Our final model reached an accuracy of 75% on the validation set. We found that the subjective nature of memorability and the similarity in collected features that two pictures in different classes can have makes the data impractical to classify.

## Hyperparameter selection

<img width="444" alt="Screenshot 2022-11-18 at 15 33 18" src="https://user-images.githubusercontent.com/56508673/202741976-706b8b7d-a03b-48b7-b22f-6d31663fe4db.png">
We experimented with 6 different hyper-parameters of our RFC model and plotted their average accuracy. This provides the experimental evidence to choose the hyper-parameters of our model that will maximise its performance.

## Data re-scaling

<img width="629" alt="Screenshot 2022-11-18 at 15 33 31" src="https://user-images.githubusercontent.com/56508673/202742324-1e8c9332-911f-4aae-b551-f44e70855c47.png">
Metrical comparison of evaluated RFC models with the same hyper-parameters, trained and validated on different data sets. The impact of the training set is measured as the average accuracy- and F1-score on the validation set over 10 runs.

## Results

<img width="785" alt="Screenshot 2022-11-18 at 15 33 44" src="https://user-images.githubusercontent.com/56508673/202743131-02069e93-c7b5-426d-b00c-bb53777023fa.png">
Confusion matrix of our final model, with the only pre-processing being the imputing of missing values with the mean. The hyper-parameters were chosen through the experimentation in the section on hyperparameter selection.
