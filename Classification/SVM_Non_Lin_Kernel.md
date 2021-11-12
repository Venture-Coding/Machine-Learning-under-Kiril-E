## SVM ##  

The SVM Classifier which was earlier used for linearly separable classification can also be easily used for non-linearly separable classification.  
While the linear classification looks very similar to a Log Reg classification, the real value of SVM lies in the fact that it makes use of Maximum Margin Classification. 

So, the separator that is considered, makes use of those training examples which are classified as a certain class but are most dissimilar to that class. The model then finds all such extreme examples and then computes a linear separation that lies at such a distance from these extreme examples that it is equidistant from each of these.

Linear Separator

<img width="614" alt="Screenshot 2021-11-12 at 3 42 35 PM" src="https://user-images.githubusercontent.com/61674750/141450142-e08cd9e9-ba51-4115-87bf-d1b8ace4d2de.png">


For a non-linear classification though, such a line is not possible to be predicted at maximum margins. Hence, the model has a non-linear kernel option which projects the available data into a higher dimension such that the classes become separable with the help of a hyperplane.  
This Hyperplane is then projected back on to the earlier data dimensions, to get the non-linear curve that separates the classes. 

Non linear Separator 

<img width="655" alt="Screenshot 2021-11-12 at 3 45 57 PM" src="https://user-images.githubusercontent.com/61674750/141450639-aa2c2c3d-6961-4428-81f4-bb1b7c11e311.png">

The kernel used most widely is the Gaussian RBF Kernel. (Radial Basis Function)

<img width="699" alt="Screenshot 2021-11-12 at 3 35 48 PM" src="https://user-images.githubusercontent.com/61674750/141450719-7b6f062b-d3cb-4cbf-ae65-e19f51aeaffc.png">

### Other Types of Kernel ###

<img width="685" alt="Screenshot 2021-11-12 at 3 52 56 PM" src="https://user-images.githubusercontent.com/61674750/141451590-ca64ad00-02ff-41dc-ba7c-803fc7703cc9.png">

