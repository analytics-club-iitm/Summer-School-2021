# Assignment for Session 3
Hello everyone! Thanks for attending the third session of **Deep Learning Master-Class**. We hope you enjoyed the session. To consolidate upon the concepts learnt, you will be implementing **Support Vector Machines (SVMs)** on the Titanic dataset as the assignment for this session.
## Dataset
The Dataset to be used in the assignment is the popular *Titanic Dataset*. It presents a binary classification task, wherein we have to predict if a particular person will survive the Titanic shipwreck given a set of features.
## Support Vector Machines
SVMs are a supervised learning algorithm, and can be used for classification as well as regression. SVMs are quite useful, being memory efficient and having a versatile choice of kernels. In the following task, you will be experimenting with two kernels: *linear kernel* and *rbf (Radial Basis Function) kernel* and finding the best set of hyperparameters for each of them.
## Task
*Read all the step-wise instructions carefully. Note that all submissions are to be made via a Google form, the link for which is given in the following section.*
1. Load the zipped folder [Datasets.zip](Datasets.zip) which contains the training and test datasets.
2. After performing data cleaning on the training set, generate *any three visualisations for the data of your choice.* For data cleaning, you may refer to the session notebook for [logistic regression](https://colab.research.google.com/drive/1we-KLioF8qVjVXsB13tORjQALJYjSHLG?usp=sharing). Save the generated images in .jpg/.png format, and submit the three images in the Google form.
3. Construct a binary classifier for the *Titanic dataset* using the **sklearn.svm.SVC class**. Details follow in the subsequent points.
4. In the above task, use the *linear* and *rbf* kernels. Each of the two kernels has one or more hyperparameters associated with it. You are expected to find the best set of hyperparameters for each of the two kernels. Use GridSearchCV on the training dataset for this purpose. The hyperparameters expected to be tuned for each of the kernels are: 
    1. **Linear Kernel:** C
    2. **rbf Kernel**: C and gamma
5. Report the best hyperparameter values for each of the kernels in the submission Google form. *(Think: How will you feed in a wide range of values for each hyperparameter to GridSearch, while ensuring that the total number of values is not too large for execution of GridSearch in reasonable time? Answer given in the bottom.)* 
6. Make predictions for the test dataset using each of the two kernels along with the best parameters obtained from the previous step. Submit your predictions for the test dataset, one for each of the two kernels in csv format. Note that the submission should have a single column with the predicted values *(use index=False while saving the predictions using .to_csv)*.
7. Submit your code as well.
8. **Optional:** Try using other kernels like *poly, sigmoid* and report the best hyperparameters for those.
## Making the submission
Make your submissions in this [Google form.](https://forms.gle/JT2CJJ9wZbsPBkD17)  
**Deadline** for the submission is **EOD Tuesday, 13th July**
## Supporting Material
The following references can be used for the stated purposes:
* [An article to understand SVM basics, mathematical intuition, need for kernels and an overview of hyperparameters involved](https://towardsdatascience.com/svm-and-kernel-svm-fed02bef1200)
* [Documentation for sklearn.svm.SVC](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)
* [GridSearchCV explanation and implementation](https://towardsdatascience.com/gridsearchcv-for-beginners-db48a90114ee)
* Bonus (not required to solve the assignment): [A tutorial to understand the rigorous mathematical formulation of SVMs](https://www.svm-tutorial.com/2014/11/svm-understanding-math-part-1/)
* You may also refer to the relevant theory given at the end of the [session notebook](https://colab.research.google.com/drive/1CekCToXAKB7Ife1r1Ya8Vz9PfDpUjuA3?authuser=1#scrollTo=hXMRQgBgWXgR).

All the best for the task! Feel free to reach out to us in case of any doubts.

*Answer to the question: Initially feed the hyperparameter ranges in a log scale to GridSearchCV, e.g. [1,10,100,1000]. A linear scale can then be used for further refinement.*
