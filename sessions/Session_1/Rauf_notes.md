## Main Idea of the Paper
- the paper questions how we actually understand generalization in deep neural networks.
- Normally, we think that bigger models have more capacity, so they can easily overfit the training data and perform poorly on unseen data.
- However, the authors show that deep neural networks can also fit completely random labels, meaning they have enough capacity to memorize training data even when there is no meaningful relationship between inputs and labels.
## Experiments & Results
- The authors experiment with different datasets, architectures and randomization settings.
- They change labels or even randomize input images to test the memorization ability of neural networks.
- Their results show that networks can achieve almost zero training loss, even when labels are random or images are randomized.
- When labels become increasingly corrupted:
  - Training takes longer.
  - Test error increases.
- This shows that memorization and generalization are two different things. A model can perfectly fit its training data but still perform poorly on unseen data.
## My Understanding / Takeaway
- The ability of neural networks to memorize data is not necessarily the main problem.
- The bigger question is why neural networks prefer learning useful patterns from real data instead of simply memorizing it.
- Neural networks can represent almost any labeling of a finite training dataset, yet they still generalize well in many real world tasks.
- The reason behind this behaviour is still not fully understood.