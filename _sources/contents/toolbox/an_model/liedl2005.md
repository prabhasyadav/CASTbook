## CAST Toolbox - Analytical Models - Liedl et al. (2005)

(des_li2005)=
### Liedl et al. (2005) model ### 

This model, based on [Liedl et al. (2005)](refli2005), provides an estimate of a steady-state plume length ($L_{max}$ ) from a vertically oriented 2D model domain (see {numref}`li2005_1`). The vertical orientation refers to $z$-axis being aligned to the aquifer thickness. 

```{figure} images/li2005/liedl2005fig.png
---
scale: 40%
align: center
name: li2005_1
---
The Liedl et al. (2005) model
```

[Liedl et al. (2005)](refli2005) provides the following explicit expression for $L_{max}$:

$$
L_{max} = \frac{4}{\pi^2}\frac{M^2}{\alpha_{Tv}}\ln\bigg(\frac{4}{\pi}\frac{\gamma C_{ED}^\circ + C_{EA}^\circ }{C_{EA}^\circ}\bigg)
$$

```{sidebar} in which: 
$M$ = Source Thickness [L], which is equal to Aquifer thickness ($A_t$) [L]<br/>
$\alpha_{Tv}$ = Vertical Transverse Dispersivity [L]<br/>
$\gamma$ = Reaction stoichiometric ratio [ ]<br/>
$C_{ED}^\circ$ = Contaminant (Electron Donor) concentration [ML$^{-3}$]<br/>
$C_{EA}^\circ$ = Partner Reactant (Electron Acceptor) concentration [ML$^{-3}$]
``` 

**The model is based on the following assumptions:**

1. Steady-state condition in a homogeneous and isotropic aquifer.
2. A single step bi-molecular instantaneous reaction between reactants taking place only at the fringe.
3. The contaminant source (Electron Donor) penetrates entire thickness of the aquifer.
 
(refli2005)= 
#### Reference: #####
Liedl, R., Valocchi, A., Dietrich, P., Grathwohl, P., 2005. Finiteness of steady state plumes. Water Resour. Res. 41, W12501. https://doi.org/10.1029/2005WR004000


### Using Liedl et al. (2005) model in CAST


Clicking the **Analytical Toolbox** box in the homepage will lead to the interface that lists ({numref}`li2005_2`) all the analytical models available in the CAST. To use the Liedl et al. (2005) model. From the interface, please click on the option **`Click here to see the model`** below the Liedl et al. (2005) as shown on the  screenshot ({numref}`li2005_2`).


```{figure} images/li2005/li2005_0.png
---
scale: 50%
align: center
name: li2005_2
---
The listing of Analytical models of CAST and selection of Liedl et al. (2005) model.
```


By doing so, you will be directed to this page, which contains a brief description of this model - as is provided [here](des_li2005). The screenshot below ({numref}`li2005_3`) shows the interface 

```{figure} images/li2005/li2005_1.png
---
scale: 40%
align: center
name: li2005_3
---
Interface describing Liedl et al. (2005) model.
```

Please click on option **Liedl et al. (2005)**, located in the _top_ bar, to open the dropdown menu containing the **two** options for computation (see {numref}`li2005_4`. 
In case a user wishes to model a single site or a number of sites but one at a time **`Single computing simulation`** option can be used. And if the number of sites is more than one or a user wishes to model the several sites or scenarios at once, then **`Multiple computing simulation`** option can be used. 


```{figure} images/li2005/li2005_2.png
---
scale: 40%
align: center
name: li2005_4
---
Computation options in CAST
```

### Using Single Computing Model of Liedl et al. (2005) in CAST ###

The **single computing simulation** interface is activated when it is clicked. as in the screenshot {numref}`li2005_5`. 


After clicking on **`single computing simulation`**, you will be directed towards the below attached window ({numref}`li2005_4`). The area highlighted in red square in {numref}`li2005_4` contains the _input_ parameters for the model which are briefly defined below:


**`Thickness` ($M$):** refers to the aquifer thickness (in m). In [Liedl et al. (2005)](refli2005) $M$ is the most sensitive quantity affecting $L_{max}$  


**`Dispersivity`** ($\alpha_{TV}$): refers to the transverse vertical dispersivity (in m). It affects the mixing intensity of the liquid phase along the vertical axis. This is a highly sensitive parameter, with strong impact on the $L_{max}$.


**`Stoichiometric Ratio`** ($\gamma$): is unitless parameter dependent on the contaminant compound and its reaction partner. 


**`Electron Donor`** ($C_{ED}$):refers to the contaminant source concentration (in mg/l).


**`Electron Acceptor`** ($C_{EA}$): refers to the concentration of the dominating reactant e.g., Oxygen (mg/l).


```{figure} images/li2005/li2005_3.png
---
scale: 40%
align: center
name: li2005_4
---
The single computing interface of CAST.
```

In order to change the values of any of the input parameters, please move your cursor next to the data entry fields and use navigator arrows to increase or decrease the value (see {numref}`li2005_4`. You can also directly enter the required value in the field.
Finally, when you have defined the input parameters as per your requirement, please click on the **`Generate Graph`** option.
By doing so, the system will generate a new graph that includes the new $L_{max}$ based on the newly defined parameters. Also, the system provides the value of $L_{max}$  at the bottom as shown in the screenshot {numref}`li2005_4` . 

After the firs computation and graph generated, an interactive _sliders_ appears in the interface (see {numref}`li2005_5`). These slider can be used for changing the values of  **`Thickness`** and **`Dispersivity`** that appear below the **`Maximum Plume Length`**,as shown in the above screenshot {numref}`li2005_4`, to see how the $L_{max}$ changes upon changing these parameters. 

```{figure} images/li2005/li2005_4.png
---
scale: 40%
align: center
name: li2005_5
---
Interactive option in the single computing interface of CAST
```

```{attention}
The sliders will only appear after the first computation is made.
```
In case you wish to see the graph on _Fullscreen_ mode, please click on the button **`view full screen graph`**.


Moving your cursor to the top right corner of the generated **graph** will reveal the advanced options bar (see {numref}`li2005_6`). These options enable you to download/export and interact with the graph.

```{figure} images/li2005/li2005_5.png
---
scale: 40%
align: center
name: li2005_6
---
Interactive option in the single computing interface of CAST
```

The interactive options available with graphs are:
`Zoom`, `Pan`,`Box Select`, `Lasso Select`, `Zoom in_ and _Zoom out`, `Auto scale`, `Reset Axes`, `Toggle spike lines`, `Show closest data on hover`, and `Compare data on hover`.

### Using Multiple Computing Simulation for Liedl et al. (2005) model ###

**`Multiple computing mode`** is suitable for _scenario based modeling._ In this one can create several scenarios by changing model input parameters and obtain $L_{max}$ for all scenarios at ones. This helps comparing between different created scenarios.    

Now, in case a user wants to use the **`Multiple Computing Simulation`**, one need to click on the option, located in top bar, as seen in {numref}`li2005_7`.

```{figure} images/li2005/li2005_6.png
---
scale: 40%
align: center
name: li2005_7
---
Selecting Multiple Computing Simulation option
```

By doing so, you will be directed to this screen where you can select/upload multiple sites for your analysis. 
You can select sites from the already existing _dataset_ for which please click on **`All sites button`**, as seen in {numref}`li2005_8` . Upon clicking, a dropdown will appear which contains a list of sites. To select the sites, please select the **`checkboxes`** adjacent to the site names, as seen in screenshot {numref}`li2005_9`. 

```{figure} images/li2005/li2005_7.png
---
scale: 40%
align: center
name: li2005_8
---
Selecting data from CAST main dataset for comparision with user data I
```

```{figure} images/li2005/li2005_8.png
---
scale: 40%
align: center
name: li2005_9
---
Selecting data from CAST main dataset for comparision with user data II
```
#### Creating multiple scenarios - offline mode ####

You can also _upload_ your own site dataset for which you have to first download _the data template_ file (a _.csv_ file). For this first you need to download the sample by clicking at **`Download Sample File`** (see {numref}`li2005_10`).  Please download the _.csv_ file and fill your data as you wish. The filling of data or creating of scenario can be done while being _offline._

```{warning}
Do not change the heading name used in sample file.
```
Once your data _.csv_ is ready, click on **`Choose File`** option, a search and select window will appear from where you can select your required file and finally click on **open** button to select it. After you have selected you file, _the file name_ will appear next to **`Choose File`** button. Next, please click on **`Upload`** button as shown on {numref}`li2005_10`, and based on the parameters defined in your file, system will generate the $L_{max}$ results on screen.

```{figure} images/li2005/li2005_9.png
---
scale: 40%
align: center
name: li2005_10
---
Providing multiple scenarios data to the CAST interface
```

The user needs to make sure that the file is in the format of the sample dataset. In such cases and in the case where the range or values of parameters don’t match the permitted, system will display an error message (see {numref}`li2005_11`). You are requested to rectify all the issues before uploading again.

```{attention} 
The online version of CAST has restricted parameter range. This is required to ensure that calculation and results are displayed with available internet requirements

For the offline version, the range can be set by user themselves.
```

```{figure} images/li2005/li2005_10.png
---
scale: 40%
align: center
name: li2005_11
---
Error message due to file format or data range in user provided data.
```

#### Creating multiple scenarios - online mode ####

For limited number of scenario data can be manually entered in the data table. This will require network connection for the online CAST. 
For addign data _manually,_ please click on the **`Add Data`** button as can be seen in screenshot {numref}`li2005_12`. 

```{figure} images/li2005/li2005_11.png
---
scale: 40%
align: center
name: li2005_12
---
Manually adding scenario data to CAST
```

By doing so, new window will appear on screen, here you can enter you data manually into the **boxes** that appears, and after entering the data in all the fields, please click on the **`Generate Graph`** button to compute. {numref}`li2005_13`

```{figure} images/li2005/li2005_12.png
---
scale: 40%
align: center
name: li2005_13
---
Manually adding scenario obtaining the results
```

If the entered values are in permitted range, system will display a message, **your entry has been added**. And based on the parameters defined, system will generate a new result graph (see below {numref}`li2005_14`). In case you wish to **delete** your results and start from fresh, please click on **`delete table data`** button, as shown in {numref}`li2005_11`.

```{figure} images/li2005/li2005_13.png
---
scale: 40%
align: center
name: li2005_14
---
Output of manually added scenarios
```

The results obtained can be download in three different formats, `.csv`, `.xls`, and `.pdf`. In case you want to print out of your results, please click on the **`print`** button, as shown on attached screenshot {numref}`li2005_15`.

```{figure} images/li2005/li2005_14.png
---
scale: 40%
align: center
name: li2005_15
---
Downloading/saving obtained results in different formats and printing results
```





