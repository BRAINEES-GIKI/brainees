# Shahmeer Session 1 Notes:

## Core argument
Large Neural Netowrks with params, that are greater than the number of examples yet they   are able to generalize well in training. and standard statistical theories fail to explain this phenomenon.  So the author trained standard CNN's(AlexNet, Inception, and MLP's) on Imagenet, and CIFAR10 Data sets with under several settings(true labels, partially corrupted labels, fully random labels, shuffeled and random pixels, and gaussian noise inplace of images). What they found  was that the Networks reached near 0pc training erorr in every case even learning all the noise, and that turning the  regularization on and off did very little to change the accuracy of the statement. Since the network is able to perform well on all types of test cases , and generalize on real ones, measures like the Rademacher complexity, and VC Dimension would be then too complex to generalize, so they r unanble to explain why deep NN's generalize then.

## Key Methodologies & Findings
standard Architectures(Inception , AlexNet on CIFAR10, Inception v3 on ImageNet) with SGD on **modified copies**(true labels,
partially corrupted labels,
fully random labels,
shuffled pixels, 
random pixels, 
Gaussian noise) of the data During these times the Hyperapramters were left unchanged between settings and mot runs had explicit regulairzation off.

**And these r some of the findings.**
1. ***Deep Neural Networks are able to easily fit random labels***: cause in very setting reached ~100pc training error, the Ones w/ the random labels, only took a bit longer to train than the true labels with no change to the learnign rate. 
2. ***Traditional statistical measures cant explain this generalization:***: 
RadeMacher complexity measures a model class's ability to fit random noise. Since these networks fit these random labels, this compelxit is ~1 which is a non-trivial  measure. Vc dimensions (is the max no. of data pts that can be correctly classified by classifier); since these NN's have such a high params count that given them enormous VC dimensions, so it will not be able to  generalize well 

3. ***Explicit Regularization is not that neccessary nor sufficient:*** From the results shown in table 1 showed that the explicit regularization techniques to train the models didn't have a huge  impact on the testing accuracy. this does not give a clear direction as to that whether generalization is acheived by regularization techniques. For example Inception trained on CIFAR10 got a  89.05pc testing accuracy but w/ regularizros off it became 85.75pc.  

4. ***Finite-Sample expressivity***: the authors constructed  this 2 layered Neural Network iwth 2n+d weights can represent any labelling of n points in d dimensions. which is a theorical match for the same principle once params have crossed the no. of data points then memorization is always possible.  this result onyl applies to a finite sample, not the whoel input domain. plus it does not say about  whether the network generalizes or that SGD woudl find those weights.
