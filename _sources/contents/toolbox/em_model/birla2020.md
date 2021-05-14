### CAST Toolbox - Empirical Models - Birla et al. (2020) ###

#### Birla et al. (2020) model description


This is a 2D empirical model, based on {ref}`Birla et al. (2020)<refbirla2020>`. The empirical model is based on the hybrid concept of combining an analytical model with an empirical function. The analytical model used is [Liedl et al. 2005](../an_model/liedl2005.md) model and empirical function is developed using MODFLOW/MT3DMS based numerical experimentation. The experimentation part uses the effect of recharge on the plume extension. The figure below provides the conceptual set-up of Birla et al. (2020).


```{figure} images/birla2020_f1.png/
---
scale: 60%
align: center
name: birla2020_f1
---
Birla et al. (2020)- conceptual set-up
```

{ref}`Birla et al. (2020)<refbirla2020>` provides the following explicit expression for $L_{max}$:

$$
L_{max} = ({1-0.047{M^.404}{R^{1.833}}})\frac{4}{\pi^2}\frac{M^2}{\alpha_{Tv}}\ln\bigg(\frac{4}{\pi}\frac{\gamma C_{ED}^\circ + C_{EA}^\circ }{C_{EA}^\circ}\bigg)
$$

```{sidebar} Symbols:
$M$ = Source Thickness [L], which is equal to Aquifer thickness ($A_t$) [L]<br>
$\alpha_{Tv}$ = Vertical Transverse Dispersivity [L]<br>
$\gamma$ = Reaction stoichiometric ratio [ ]<br>
$C_{ED}^\circ$ = Contaminant (Electron Donor) concentration [ML$^{-3}$]<br>
$C_{EA}^\circ$ = Partner Reactant (Electron Acceptor) concentration [ML$^{-3}$]<br>

$R$= Recharge rate [L$^{3}$T$^{-1}$]
```

**The model is based on the following assumptions:**

1. Steady-state condition in a homogeneous and isotropic aquifer.
2. A single step bi-molecular instantaneous reaction between reactants taking place only at the fringe.
3. The contaminant source (Electron Donor) penetrates entire thickness of the aquifer.
4. Recharge is uniform thorughout the domian and is continuous.


#### Using Birla et al. (2020) model in CAST ####

Clicking the **Empirical Toolbox** box in the homepage ({numref}`birla_f1a`) will lead to the interface that lists all the empirical models available in the CAST. To use the Birla et al. (2020) model from the interface shown in the screenshot below, please click on the option ``Click here to see the model`` below the Birla et al. (2020) as shown on the screenshot below.

```{figure} images/birla2020_f1a.png
---
scale: 60%
align: center
name: birla_f1a
---
Selecting an empirical model
```

##### Single computing interface #####

The CAST user-interface is identical for both the analytical as well as empirical models which makes it more user-friendly. This is true for both single computing interface and multiple simulation interface. Therefore, the extensive details on using the [Liedl et al. (2005)](../an_model/liedl2005.md) model in CAST can also be used for the Birla et al. (2020).

The only difference in each model interface lies in the model specific parameters. This can be observed in the CAST screenshot below: 

```{figure} images/birla2020_f2.png
---
scale: 50%
align: center
name: birla_f2
---
Parameters required in Birla et al. (2020) model
```

After all the required fields are filled up, a user needs to click on the  **``Generate Graph``** to get the result. Results are obtained as an absolute number below the ``Generate Graph`` button and also graphically, which provides the field plume length data from the database. This allows a visual comparison of the model $L_{max}$with the field data.

As explained in detail in the analytical model [Liedl et al. (2005)](../an_model/liedl2005.md), the resulting graph provides several interactive options to evaluate results. The screenshot below provides the output of the single computing mode of CAST.

**Dynamically comparing model results - using sliders**

Sliders (see {numref}`birla2020_f2`) become activate only after the **``Generate Graph``** is clicked (see Interactive options in the Single computing interface). Sliders are provided for more critical model parameters that have been suggested in Birla et al. (2020) paper. Sliders changes the model input parameters; for which the output $L_{max}$ appears in the graph. This enables a dynamic computation and visualization. 

##### Multiple computing interface #####

The multiple computing interface of the Birla et al. (2020) model is identical to the  interface of analytical model [Liedl et al. (2005)](../an_model/liedl2005.md). The goal of the multiple computing interface is to develop several scenarios and compare the output of these scenarios with that of the field data. As can be observed in the screenshot below, users have an option to select the site(s) they would like to compare their scenarios with.

```{figure} images/birla2020_f3.png
---
scale: 60%
align: center
name: birla_f3
---
Selecting site to compare using multiple computing interface of CAST
```

The interface of multiple computing interface is provided in the screenshot below. Details on the options are identical to that provided for [Liedl et al. (2005)](../an_model/liedl2005.md). The screenshot below is for clarification.


```{figure} images/birla2020_f4.png
---
scale: 60%
align: center
name: birla_f4
---
Available options for extracting model results from CAST interface.
```


(refbirla2020)= 
#### Reference #### 

Birla, s., Yadav, P.K., Mahalawat, P., Haendel, F., Liedl, R., Chahar, B. 2020. Influence of recharge rates on steady-state plume lengths. Jour. Contam. Hydrol. https://doi.org/10.1016/j.jconhyd.2020.103709


