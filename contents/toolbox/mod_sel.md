### CAST Toolbox - Model Selection method

**The Model Selection toolbox is not implemented in the CAST yet**. 
The most important reason for that is the very limited information available on this subject. The text below outlines some development on the _Model Selection Method,_ and the current progress.

CAST provides several models of different types (analytical, numerical and empirical/hybrid). 
The key question then is, which model to start with at a particular site?  

Normally using a model that requires many input parameters may not be the best choice to start modeling works.
Typically, information requirements are higher for models with higher dimension (3D) and numerical models. Also, lower dimension models (<3D) but that includes several physical and (bio)chemical processes can require many input parameters.

One of the work that is being completed on _selecting a site-specific model_ is by using sufficiently large field dataset to rank models based on:

1. Statistical Threshold
2. Akaike Information Criterion (AIC)
3. Analytical Hierarchy Process (AHP)

The **Statistical Threshold** ($ST$) method ranks model based on model's ability _overestimate,_ _underestimate,_ and _overly-overestimate_ the field plume length. _Overly-overestimate_ which is often provided by 2D models (Liedl et al., 2005), is considered a model failure. The $ST$ method thus requires providing the **threshold** for the _overly overestimate_

**AIC** approach in addition to model complexity requires **weights** for model underestimation and overly overestimation, both model failures. The **weights** are site-specific conditions.

**AHP** is full-scale multi-criteria model ranking approach. The **weights** of each selected criteria is required to provided. In the current development 4 models with 4 criteria is being tested.

The current works on the _model selection method_ can be visualized by the following flow-chart. 

```{figure} images/dec_model_f1.png
---
scale: 80%
align: center
name: dec_model
---
Flow-chart on approach for selecting site-specific decision model.
```

The flow-chart provided above can be fully automated. Furthermore, it can be linked with data toolbox of CAST.