# SAMI: SESSION 01 NOTES
The ability of a model to generalize well on test data shows how credible its results can be in real life. But what exactly is the thing that separates a model that generalizes well from one that does not?

This paper does not suggest its own method to find out that particular point rather it explores the already existing beliefs about generalization and tells us if they are credible enough or not. When this paper was written there were two common traditional beliefs about what defined the generalization capability of a model: 

1- _Depth of the model architecture_  
2- _Regularization techniques using during training_

The researchers performed different experiments to disprove these traditional claims

### EXPERIMENTS AND RESULTS

#### Randomization Tests:
For this part the researhers trained models with deep architctural details (like inception, MCP, Alexnet) on a dataset with randomized labels. They noticed that almost all of the models were able to reach convergence during training even if it took them more time compared to true labels.

They found out that all the models had **100% accuracy on training data** but when tested on testing data it was found out that _the more the labels were corrupted the less the accuracy got_ minimizing at 10% on CIFAR-10 data.
This showed that the models failed poorly to generalize and hence disproved the first claim. Showing that neither depth nor the family of model had any impact on generalization

#### Explicit Regularization:
Then they set out to find the impact of regularization on generalization ability. They considered explicit regularization techniques like weight decay, data augmentation and dropout layers.

But the results shown in table 1 tell us that the regularization techniques used to train multiple kinds of models **did not have huge impact on testing accuracy** the accuracy varied a little bit whihc does not give any useful information that generalization is acheived by regularization techniques. Hence disproving the second traditional belief.

#### Implicit Regularization:
They also tried techniques for implicit regularization like **early stopping** and **batch normalization**  
They did not find any potential benefit of early stopping on their dataset. Batch norm has just minimum impact on generalization performance  but isnt on its own the main reason for generalization

#### Finite Sample Expressivity:
Researchers constructed their own neural network that can represent any function on a sample size n in d dimensions  
The total number of parameters in this network were given as p = 2n+d. Hence the parameters were greater than the number of samples. Showing that even e neural network with this simple architecture can fit finite arbitrary data points.

### Challenges for traditional statistical theories:
#### VC Dimension:
It refers to the maximum number of data points that can be classified correctly by a classifier. For example, the VC dimension of a straight line is 3  
The researchers demonstrated that if a simple neural network (like the one they built) can fit huge number of finite samples then deep neural networks have far more parameters hence their fitting capability is far greater means their VC dimension will be huge. That shows that VC dimension cannot guarantee the generalization ability.

#### Rademacher Complexity:
It refers to the amount of random labels that a model can fit properly. High Rademacher complexity means hypothesis can fit random patterns very well. Low means it cannot fit random patterns well. It varies from 0-1.  
So according to the experiments when a model is trained on a randomized label dataset it fit the labels very well giving 100% training accuracy which means Rademacher Complexity = 1 this weaknes the generalization guarantee as seen in the Randomized tests section. Hence rademacher complexity also does not define generalization capability

#### Uniform Stability:
Uniform stability means how much the performance of a model changes if we just replace one training sample with another. If the performance remains similar it means that the model algorithm is stable. If there is a huge difference the algorithm is unstable.  
But algorithms stability alone doesnt explain the difference between learning meaningful patterns and memorizing random labels.  



After this, the authors moved towards linear models. As finding the reason for generalization in neural networks can be complex so they thought that they might find something in linear models that can be associated with generalization of neural networks. They found out that for nxd matrix if d>=n there can be multiple solutions. But the problem was to find if all solutions generalize equally well. But after investigating they found no such meaningful result that could be associated with the generalization of neural networks.