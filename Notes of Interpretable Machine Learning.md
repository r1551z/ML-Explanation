https://christophm.github.io/interpretable-ml-book/index.html

# chapter 2

**Interpretability is the degree to which a human can understand the cause of a decision.**

## why

## Taxonomy of Interpretability Methods (different type of model explanation)

          feature summary 

          feature summary visualization

          model internal parameters

          Data point

          Intrinsically interpretable model:
          
            
    
    
### Data point: 

This category includes all methods that return data points (already existent or newly created) 
to make a model interpretab. One method is counterfactual explanations. Another is the 
identification of prototypes of predicted classes

### Intrinsically interpretable model
One solution to interpreting black box models is to approximate them 
(either globally or locally) with an interpretable model. 
The interpretable model itself is interpreted by looking at 
internal model parameters or feature summary statistics.

## 2.3 Scope of Interpretability

algorithm; global (holistic, modular level), local (single prediction, a group of 
predictions)


## Evaluation of Interpretability

### Application level evaluation (real task):
It means to ut the explanation into the product and 
have it tested by the end user.
It requires experiment setup and understanding how to assess quality.
A good baseline for this is always 
how good a human would be at explaining the same decision

### Human level evaluation (simple task)

The difference is that these experiments are not 
carried out with the domain experts, 
but with laypersons. So it will be easier and cheapter
to perform the experiments

### Function level evaluation (proxy task)
No human involvement required; 
This works best when the class of model used has already been 
evaluated by someone else in a human level evaluation.

Example:

For example, it might be known that the end users understand decision trees. 
In this case, a proxy for explanation quality may be the **depth of the tree**. 
Shorter trees would get a better explainability score. 
It would make sense to add the constraint that the predictive performance 
of the tree remains good and does not 
decrease too much compared to a larger tree.

## Properties of Explanations

**An explanation usually relates the feature values of
an instance to its model prediction in a humanly understandable way**.

### Properties of explanation methods includes:

(Expressive Power: the structure or method of explanation)

Translucency: how much the explanation relies on model parameters. High
translucency example is linear regression.

Portability: the range of ml models the method can be used. Highly portable
example is permutation importance.

algorithm complexity: how complicated the methods is.

### Properties of Individual Explanations:

accuracy: how accurate the explanation works on unseen data in terms of
prediction vs actual. it is mostly
important is the explanation / surrogation is used in place of
the model prediction.

Fidelity: How well the explanation approximate 
the prediction of the black box model. **If the black box model has high 
accuracy and the explanation has high fidelity, 
the explanation also has high accuracy. **

Consistency: how much does an explanation differ between models 
that have **been trained on the same task** and that **produce similar predictions**.
High consistency is desirable if the models really rely on similar relationships.

Stability: 
stability compares explanations between similar instances for a fixed model.
**High stability means that slight variations in the features 
of an instance do not substantially change the explanation**, unless
that change also drastically changes the prediction.

High stability is always desirable.







