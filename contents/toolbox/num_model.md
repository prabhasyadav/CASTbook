## CAST Toolbox - Numerical Model
### 1 Model Description
The numerical model in the CAST is based on the conceptual work presented in [Yadav et al. (2014)](des_num). The 2D numerical domain is vertically orineted and follows the assumptions similar to that provided in [Liedl et al., (2005,)](des_num), e.g., homogeneous, isotropic, steady-state and bi-component (Electron Donor or contaminant concentation *C<sub>ED</sub>* and Electron Acceptor or the partner reactant concentration *C<sub>EA</sub>*) instantaneous reaction (see [Liedl et al., 2005](des_num) Analytical Model of the CAST- **to be linked**).  

```{figure} images/num_f1.png
---
scale: 60%
align: center
name: num1
---
Numerical model conceptual set-up
```
  
**MODFLOW** and **MT3DMS** are used in the simulation, which provides contour of a transformed concentration, *C(x,z)*. The transformed concentration, based on Yadav et al. (2014), enables simulation of reactive system (*C<sub>ED</sub>* and *C<sub>EA</sub>*) as a conservative system. The maximum plume length (*L<sub>max</sub>*) is then the distance between the source (the left edge of the domain) and the largest distance of the chosen threshold concentration (e.g., *C=0*) along *x*−axis.  
  
Complete details of **MODFLOW** used for flow simulations from [here](https://www.usgs.gov/software/modflow-2005-usgs-three-dimensional-finite-difference-ground-water-model), and that of the **MT3DMS** required for transport simulations can be obtained from [here](https://hydro.geo.ua.edu/). Furthermore, FloPy (see [here](https://www.usgs.gov/software/flopy-python-package-creating-running-and-post-processing-modflow-based-models)) is used for implementing numerical model in CAST interface.

The numerical approch for solving transport related groundwater problems comes with the advantages of being adaptable to many different cases regarding their individual case features aswell as high accuracy. However this also comes with an increased computing effort, mainly dependent of the number of cells used for the model. Very fine meshes result in high computing times, which may not be suitable for the online version of the tool. It is recommended to start simulating with rather coarse meshes and then refining them after. Also an offline version can be downloaded which can be used if very fine meshes for very high accuracy are wanted. The offline version also does not restrict parameter ranges in any way. ***(I am not sure what the up to date ranges are we are using - This is to done once Vedanti is active)***  

### 2 Input Parameter
The following section provides an overview over all required parameters for the numerical model and their specific functions. The cases provided in the database of this tool are characterized by most of those parameters. However due to the requirement of many paramters in the numerical model, some of them (e.g. Dispersivities) may not be found. Due to those parameters being difficult to aquire in many cases, default values are provided to use in the model.  

### 2.1 System Parameters
***Length*** - defines the extend (in m) of the model domain in _x_-dircetion i.e. the direction of groundwater flow. For large domains an adequat number of columns must be assigned which may result in slightly longer calculation times.  
***Height*** - refers to the thickness (in m) of the aquifer, which is also assumed to be the vertical extend of the contamination within the aquifer.  
***Number of Rows*** - specifies the amount of cells which the domain is divided into, along the vertical axis. Since the model result is strongly influenced by the vertical discretization, a cell width of 0.1 m is recommended to obtain accurate results.  
***Number of Colums*** - specifies the amount of cells which the domain is divided into, along the x-axis. A cell length of 10 m was found to be optimal for the purposes of both accuracy and efficiency.  

{numref}`num2` provides the screenshot of system parameters input interface of the CAST.

```{figure} images/num_f2.png
---
scale: 40%
align: center
name: num2
---
Numerical model system parameters
```
### 2.2 Hydraulic Parameters

***Head inlet*** - represents a first order boundary condition needed to satisfy the model requirements for calculating groundwater flow. It is given as a constant hydraulic head (in m) at the domain extned of *x=0*.  
***Head outlet*** - represents the second required first order boundary condition, located at *x = domain end*. The value of *head outlet* must be less than *head inlet* to ensure a groundwater flow in positive x-direction. The hydraulic gradient of the model domain is hence given as a combination of the paramters *Length*, *Head inlet* and *Head outlet*. 

$$i=\frac{Head\ outlet - Head\ inlet}{Length}$$

***Porosity*** - is the value of the effective porosity of the ground matrix.  
***Conductivity*** - defines the hydraulic conductivity of the aquifer in m/s.  
***Longitudinal Dispersivity*** - is an aquifer parameter which effects the intensity of mixing in the liquid phase along the x-axis. The default value is 10 m.  
***Transverse Vertical Dispersivity*** - effects the mixing intensity of the liquid phase along the vertical axis. This is a highly sensitive parameter, with strong impact on the maximum plume length. The default value is 0.01 m.  

### 2.3 Chemical Parameters

***Contaminant Concentration*** - refers to the source concentration of the contamination. It is given in mg/L

***Partner Reactant Concentration*** - refers to the concentration of the dominating reactant e.g. Oxygen. 

***Stoichiometric Ratio*** - is dependent on the contaminant chemical form, e.g., Benzene, and its reaction partner, e.g., Oxygen. It defines the ratio of consumption of each compound when reacting. This value, a constant, can be found tabulated in standard chemistry book.


{numref}`num3` provides the screenshot of hydraulic and chemical parameters input interface of the CAST.

```{figure} images/num_f3.png
---
scale: 40%
align: center
name: num3
---
Numerical model hydraulic and chemical parameters
```

### 3 Model Output
The model output is given as the maximum plume length as well as a plot of the plume fringe within the two dimensional vertical domain. The area under the curce represents the contaminant plume, where the concentration of the $C_{ED}$ dominates. The area above the curve is dominated by the $C_{EA}$, where no contamination is found. $L_{max}$ is the maximum extent of $C_{ED}= C_{EA}$ curve.

{numref}`num4` provides the screenshot of the model output from CAST.

The obtained output can be saved as a *.png* file.


```{figure} images/num_f4.png
---
scale: 40%
align: center
name: num4
---
Numerical model output
```

(des_num)=
### References

Yadav, P. K., Liedl, R., and Dietrich, P. (2014). Influence of source thickness on steady-state plume length. Environ. Earth Sci., 71(2), 959-964. https://doi.org/10/f5qfwm28 

Liedl, R., Valocchi, A. J., Dietrich, P., and Grathwohl, P. (2005), Finiteness of steady state plumes, Water Resour. Res., 41, W12501, doi:10.1029/2005WR004000.
