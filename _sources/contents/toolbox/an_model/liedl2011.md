#### CAST Toolbox - Analytical Models - Liedl et al. 2011 ####
{ref}`Liedl et al. 2011 <ref1>`
{ref}`Liedl et al. <ref2>`
**Prabhas** to do this.


##### **4.  <u>3D</u> Model**  – Liedl et al. (2011) #####

This model, based on Liedl et al. (2011)<sup>[^Liedl2011]</sup>, provides an estimate of a steady-state plume length ($L_{max}$ ) from a 3D model domain (see figure). This model extends the 2D model present in Liedl et al. (2005). As is in the 2D model, in this model too the vertical orientation refers to $z$-axis being aligned to the aquifer thickness. The domain width and length is infinite in this model.


```{figure} images/an_li2011_f1.png
---
scale: 40%
align: center
name: li2011
---
Liedl et al. (2011)- Conceptual problem
```
Liedl et al.(2011) provides the following explicit expression for $L_{max}$:

```{sidebar} Symbols:
$M$ = Source Thickness [L], which is equal to Aquifer thickness ($A_t$) [L]<br/>
$\alpha_{Tv}$ = Vertical Transverse Dispersivity [L]<br/>
$W$ = Source Width [L]<br/>
$\alpha_{Th}$ = Horizontal Transverse Dispersivity [L]<br/>
$\gamma$ = Reaction stoichiometric ratio [ ]<br/>
$C_{ED}^\circ$ = Contaminant (Electron Donor) concentration [ML$^{-1}$]<br/>
$C_{EA}^\circ$ = Partner Reactant (Electron Acceptor) concentration [ML$^{-1}$]<br/>
$C_{Thres}$ = Threshold Contaminant Concentration [ML$^{-1}$]
``` 

$$
\text{erf}\bigg(\frac{W}{\sqrt{4\alpha_{Th}L}}\bigg)\,\text{e}^{-\alpha_{Tv}L \big(\frac{\pi}{2M}\big)^2} =\frac{\pi}{4}\frac{\gamma C_{Thres}+C_{EA}^\circ}{\gamma C_{ED}^\circ+C_{EA}^\circ}
$$



The $C_{Thres}$ in this model allows to set the contaminant concentration to any value greater than or equal to zero, and then $L_{max}$ is length from the origin to that maximum distance of $C_{Thres}$ along $x$-axis . 

**The model is based on the following assumptions:**

1. Steady-state condition in a homogeneous and isotropic aquifer.
2. A single step bi-molecular instantaneous reaction between reactants taking place only at the fringe.
3. The contaminant source (Electron Donor) penetrates entire thickness of the aquifer.
 
**Reference:**

```{admonition} Click the button to reveal!
:class: dropdown
Some hidden toggle content!

![](images/an_li2011_f1.png)
```


```{toggle}
Some hidden toggle content!

```{figure} images/an_li2011_f1.png
---
scale: 40%
align: center
name: li2011
---
Liedl et al. (2011)- Conceptual problem

```

(ref1)=
[^Liedl2011]: Liedl, R., Yadav, P.K., Dietrich, P., 2011. Length of 3-D mixing-controlled plumes for a fully penetrating contaminant source with finite width. Water Resour. Res. 47. https://doi.org/10.1029/2010WR009710 

(ref2)=
Liedl, R., Yadav, P.K., Dietrich, P., 2011. Length of 3-D mixing-controlled plumes for a fully penetrating contaminant source with finite width. Water Resour. Res. 47. https://doi.org/10.1029/2010WR009710 
