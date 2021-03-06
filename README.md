Practical-Machine-Learning-Course-Project
======================================================
-This project is to apply the machine learning algorithm to each of the 20 test cases in the testing data set. 
For each test case to submit a text file with a single capital letter (A, B, C, D, or E) 
corresponding to prediction for the corresponding problem in the test data set. You get 1 point 
for each correct answer. You may submit up to 2 times for each problem. It is a lot of files to 
submit. It may be helpful to use the following function to create the files. If you have a 
character vector with your 20 predictions in order for the 20 problems.

-Six young health participants were asked to perform one set of 10 repetitions of the Unilateral Dumbbell 
Biceps Curl in five different fashions: exactly according to the specification (Class A), throwing the 
elbows to the front (Class B), lifting the dumbbell only halfway (Class C), lowering the dumbbell only 
halfway (Class D) and throwing the hips to the front (Class E).
Class A corresponds to the specified execution of the exercise, while the other 4 classes correspond to 
common mistakes. Participants were supervised by an experienced weight lifter to make sure the execution
complied to the manner they were supposed to simulate. The exercises were performed by six male participants
aged between 20-28 years, with little weight lifting experience. We made sure that all participants could 
easily simulate the mistakes in a safe and controlled manner by using a relatively light dumbbell (1.25kg).
Read more: http://groupware.les.inf.puc-rio.br/har


##The following plots are random forest, gbm and knn fitted accuracies from training dataset with 5 folds cross validations.
![plot of random-forest](random-forest.png)
```{r 1,fig.width=4,fig.height=3,message=FALSE}
library(png)
img <- readPNG("random-forest.png")
grid::grid.raster(img)
```

![plot of gbm](gbm.png)

```{r 2,fig.width=4,fig.height=3,message=FALSE}
library(png)
img <- readPNG("gbm.png")
grid::grid.raster(img)
```

![plot of knn](knn.png)

```{r 3,fig.width=4,fig.height=3,message=FALSE}
library(png)
img <- readPNG("knn.png")
grid::grid.raster(img)
```  

 
##The following lists are some classification results on the dataset
```{r}
rx <- read.table("results.txt")
colnames(rx) <- c("matches","methods")
rx
```
