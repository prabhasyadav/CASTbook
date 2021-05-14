### CAST Toolbox - Analytical Models


The analytical model toolbox within the CAST provides the solution for $L_{max}$. The toolbox currently include **6** different models; each of them varying with the other with respect to model conditions, dimensionality, input quantities, and also orientation. Analytical model toolbox is the recommended step after the use of _Data Toolbox_ in the CAST work flow.

#### Analytical models in CAST ####
Included models are (_see individual model page for details_):

1. [Ham et al. (2004)](./ham2004.md) 

    $$
  L_{max} = \frac{W_r^2}{4\pi\alpha_{Th}}\bigg(\frac{\gamma C_D^\circ}{C_A^\circ}\bigg)^2 
  $$
2. [Liedl et al. (2005) ](./liedl2005.md)

    $$
 L_{max}\frac{4M^2}{\pi^2 \alpha_{Tv}}\ln\bigg( \frac{4}{\pi}  \frac{\gamma C_{ED}+ C_{EA}}{C_{EA}}\bigg)
$$

3. [Chu et al. (2005)](./chu2005.md)

    $$
 L_{max} = \frac{\pi}{16}\frac{W^2}{\alpha_{Th}} \Bigg(\frac{\gamma C_D^\circ }{C_A^\circ -\epsilon}\Bigg)^2 
$$

4. [Liedl et al. (2011)](./liedl2011.md)

    $$
\text{erf}\Bigg(\frac{W}{\sqrt{4\alpha_{Th}L_{max}}}\Bigg)\,\text{e}^{-\alpha_{Tv}L_{max} \big(\frac{\pi}{2M}\big)^2} =\frac{\pi}{4}\frac{\gamma C_{Thres}+C_{A}^\circ}{\gamma C_{D}^\circ+C_{A}^\circ}
$$
5. [Karanovic et al. (2007) - **BIOSCREEN-AT**](./bioscreen.md)

    $$
c(x,y,z, t) = C_0 \frac{x}{8\sqrt{\pi D_x'}}\exp(-\gamma t) 
\times \int\limits_0^t\frac{1}{\xi^{3/2}}\exp\Bigg\{(\gamma-\lambda_{EFF})-\xi \frac{(x-v'\xi)^2}{4D_x'\xi}\Bigg\}
\times
$$

$$\times \Bigg[\text{erfc}\Bigg\{\frac{y-\frac{w}{2}}{2\sqrt{D_y'\xi}}
\Bigg\}-\text{erfc}\Bigg\{\frac{y+\frac{w}{2}}{2\sqrt{D_y'\xi}}
\Bigg\}\Bigg]\times$$

$$\times \Bigg[\text{erfc}\Bigg\{\frac{z-H}{2\sqrt{D_z'\xi}}\Bigg\}
\text{erfc}\Bigg\{\frac{z+H}{2\sqrt{D_z'\xi}} 
\Bigg\}\Bigg]\text{d}\xi$$


#### Computing interfaces in CAST ####

CAST provide the following two computing interfaces for each analytical and empirical models:

1. Single computing interface
2. Multiple computing interface

##### Single computing interface #####

The **single computing interface** is a quick computing mode in which a set of model data can be inserted in data input box to obtain $L_{max}$. The interface output (see screenshot {numref}`scm` below) is actual $L_{max}$ and the plot in which the user input result is compared against the field plume length. The output graph has limited interactive options- such as zooming, panning, and obtaining figure as a _png_ graphics. 

```{figure} images/an_f1.png
---
scale: 40%
align: center
name: scm
---
Single computing interface
```

The single computing interface also provide user interactivity with computation. Interface provide _sliders_ for changing parameter values, which leads to computation and visualization of $L_{max}$. 


##### Multiple computing interface #####

The **Multiple computing interface** provides a possibility to create simulation scenarios and compute $L_{max}$ for all scenarios at once (see screenshot {numref}`mcm` below) . Scenarios can be directly put input in the table or can be uploaded to the interface. For uploading the sample input template (a *.csv*) file has to be downloaded. After creating data in the *.csv* file, it can be uploaded to the interface for the $L_{max}$ computation. 

```{figure} images/an_f2.png
---
scale: 40%
align: center
name: mcm
---
Multiple computing interface
```
The computed $L_{max}$ is graphically displayed in the interactive figure. The obtained results can then be compared with the user selected data from the database.

The workflow with the computing interfaces can be to begin with either single or multiple interface based on the user requirements.

