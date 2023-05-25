# Training ML leakage

This is the repo for the hands-on part of the ML leakage course organized by C4DT in
collaboration with Carmela Troncoso and Bogdan Kulynych.
The training comes after a presentation from Carmela Troncoso on leakage in ML
and is split in the following parts:

1. 

How to measure vulnerability to  population attacks - 1h
In this first part, we show a very simple method to evaluate the privacy of a given ML model. We'll also see the limits of this method, namely that it is difficult to compare models based on different datasets. But you will learn how adding differential privacy to the pipeline can decrease the efficiency of a population attack.
Measuring worst-case privacy leakage in ML - 3h
A much better method is to actually measure how much of the original data can be detected in the ML model. For this, we create an IN model, where a given data was present during training, and an OUT model, where that data was not present during training. Then we can measure whether we can differentiate between the two models.
Unfortunately this approach is very computing-intensive: we have to re-create two models for every record in the original set. We will see some shortcuts which help reducing the necessary computation, while keeping usable results.
Technical details
Introduction to GitHub - privacytrustlab/ml_privacy_meter - 30'
Applying it to a given model
Create many IN- and OUT-models - 1h30
Use stochastic methods on two models (IN and OUT) only - 1h
Take home - 30'
Remind limits of Average Privacy
Summary of DP: the good and the bad
MLPrivacyMeter usage

Technical details
Population attacks
Find a model for pytorch and calculate the accuracy/loss of the training vs. the test set
What could we use as training model?
Chest X-Rays from any testing database
Any convolutional network
Average vulnerability - don't give you individual privacy measurements
Compare with the same pipeline, but
more general model (less training) would work, but probably not hold from a regulatory perspective
using Opacus (CNN) / DiffPrivLib to defend against this
take pre-trained models (normal images instead of X-Rays)
ML Privacy meter?
For the participants to calculate: the privacy attack
TPR@FPR
Teaching moment: check on accuracy, which will have a high TPR
Can compare different models on same training and test datasets


https://pastebin.com/QdB9N5B5
AUROC / AUC - https://glassboxmedicine.com/2019/02/23/measuring-performance-auc-auroc/

Other possibility: accuracy / loss -> logits, from Florian Tramèr:
https://arxiv.org/pdf/2112.03570.pdf
Next steps


Worst-case privacy leakage
use pre-trained model
calculate different models with/without the image
Take care example
Take tabular datasets with high leakage in worst-case attack, but show it can have low leakage in population attack. -> population attack low doesn't mean necessarily "all is good".

# Additional links
https://pastebin.com/QdB9N5B5 - first version of the code