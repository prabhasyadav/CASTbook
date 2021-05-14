### CAST Toolbox - Empirical Models

In CAST the **Empirical models** are those that are neither analytical nor numerical. To distinguish further **empirical models** in CAST are those that are completely based on experimentation. The experiments can be numerical, based on data, or of any other form. In general **empirical model** will thus require some fit to experimental results. Literature provide only few **empirical models**. Thus, only two empirical models are part of the current version of CAST. These are briefly presented below and explained in details in the respective model simulation sections.

#### Empirical models in CAST ####
Included models are (_see individual model page for details_):


1. [Maier and Grathwohl (2006)](mg2006.md) 

    $$
 L_{max} = 0.5\frac{M^2}{\alpha_{TV}}\bigg(\frac{\gamma C_{ED}}{C_{EA}}\bigg)^{0.3} 
  $$
2. [Birla et al. (2020) ](birla2020.md)

    $$
 L_{max} = ({1-0.047{M^.404}{R^{1.833}}})\frac{4}{\pi^2}\frac{M^2}{\alpha_{Tv}}\ln\bigg(\frac{4}{\pi}\frac{\gamma C_{ED}^\circ + C_{EA}^\circ }{C_{EA}^\circ}\bigg)
$$



#### Computing interfaces in CAST for empirical models ####

The empirical model interface of CAST can be accessed from the CAST [homepage](www.cast.iitd.ac.in). [Registration/Login](../../online/login.md) information are required for using empirical models. 

```{figure} images/em_mod_f1.png
---
scale: 60%
align: center
name: em_mod_f1
---
Accessing Empirical models toolbox in CAST
```


CAST provide the following two computing interfaces for each analytical and empirical models:

1. Single computing interface
2. Multiple computing interface

Details on these interfaces, which is identical to the interface for _analytical models_ are provided [here](../an_model/an_model.md). The screenshot provides the CAST interface to select a empirical model.

```{figure} images/em_mod_f2.png
---
scale: 60%
align: center
name: em_mod_f2
---
Selecting an empirical model
```