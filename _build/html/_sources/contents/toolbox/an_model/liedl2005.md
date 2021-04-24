## CAST Toolbox - Analytical Models - Liedl et al. (2005)

(des_li2005)=
### Liedl et al. (2005) model detail ### 

This model, based on [Liedl et al. (2005)](refli2005), provides an estimate of a steady-state plume length ($L_{max}$ ) from a vertically oriented 2D model domain (see {numref}`li2005_1`). The vertical orientation refers to $z$-axis being aligned to the aquifer thickness. 

```{figure} images/liedl2005fig.png
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
$C_{ED}^\circ$ = Contaminant (Electron Donor) concentration [ML$^{-1}$]<br/>
$C_{EA}^\circ$ = Partner Reactant (Electron Acceptor) concentration [ML$^{-1}$]
``` 

**The model is based on the following assumptions:**

1. Steady-state condition in a homogeneous and isotropic aquifer.
2. A single step bi-molecular instantaneous reaction between reactants taking place only at the fringe.
3. The contaminant source (Electron Donor) penetrates entire thickness of the aquifer.
 
(refli2005)= 
#### Reference: #####
Liedl, R., Valocchi, A., Dietrich, P., Grathwohl, P., 2005. Finiteness of steady state plumes. Water Resour. Res. 41, W12501. https://doi.org/10.1029/2005WR004000


### Using Liedl et al. (2005) model in CAST


Clicking the **Analytical Toolbox** box in the homepage will lead to the interface that lists ({numref}`li2005_2`) all the analytical models available in the CAST. To use the Liedl et al. (2005) model.


```{figure} images/Liedl1.png
---
scale: 90%
align: center
name: li2005_2
---
The listing of Analytical models of CAST
```

From the interface shown in the screenshot above, please click on the option **`Click here to see the model`** below the Liedl et al. (2005) as shown on the  screenshot below.

```{figure} images/Liedl2.png
---
scale: 90%
align: center
name: li2005_2a
---
Seclecting to use Liedl et al. (2005) model.
```

By doing so, you will be directed to this page, which contains a brief description of this model - as is provided [here](des_li2005). The screenshot below ({numref}`li2005_3`) shows the interface 

```{figure} images/Liedl3.png
---
scale: 90%
align: center
name: li2005_3
---
Interface describing Liedl et al. (2005) model.
```

Please click on option **Liedl et al. (2005)**, located in the _top_ bar, to open the dropdown menu containing the **two** options for computation (see . 
In case a user wishes to model a single site or a number of sites but one at a time **`Single computing simulation`** option can be used. And if the number of sites is more than one or a user wishes to model the several sites at once, then **`Multiple computing simulation`** option can be used. 


```{figure} images/Liedl4.png
---
scale: 90%
align: center
name: li2005_4
---
Computation options in CAST
```

### Using Single Computing Model of Liedl et al. (2005) in CAST ###

Now, in the former case, please click on the **single computing simulation** as in the screenshot {numref}`li2005_5`. 

```{figure} images/Liedl5.png
---
scale: 90%
align: center
name: li2005_5
---
Selecting the Single Compution Interface of CAST.
```

After clicking on **`single computing simulation`**, you will be directed towards the below attached window ({numref}`li2005_6`). The area highlighted in red square in {numref}`li2005_6`  contains the _input_ parameters for the model which are briefly defined below:


**`Thickness` ($M$):** refers to the aquifer thickness (in m). In [Liedl et al. (2005)](refli2005) $M$ is the most sensitive quantity affecting $L_{max}$  


**`Dispersivity`** ($\alpha_{TV}$): refers to the transverse vertical dispersivity (in m). It affects the mixing intensity of the liquid phase along the vertical axis. This is a highly sensitive parameter, with strong impact on the $L_{max}$.


**`Stoichiometric Ratio`** ($\gamma$): is unitless parameter dependent on the contaminant compound and its reaction partner. 


**`Electron Donor`** ($C_{ED}$):refers to the contaminant source concentration (in mg/l).


**`Electron Acceptor`** ($C_{EA}$): refers to the concentration of the dominating reactant e.g., Oxygen (mg/l).


```{figure} images/Liedl6.png
---
scale: 90%
align: center
name: li2005_6
---
The single computing interface of CAST.
```

In order to change the values of any of the input parameters, please move your cursor next to the data entry fields and use navigator arrows to increase or decrease the value (see {numref}`li2005_7`. You can also directly enter the required value in the field.


```{figure} images/Liedl7.png
---
scale: 90%
align: center
name: li2005_7
---
Changing input parameter value in model interface
```


Finally, when you have defined the input parameters as per your requirement, please click on the **`Generate Graph`** option.

```{figure} images/Liedl9.png
---
scale: 90%
align: center
name: li2005_9
---
Generating result and graph in single computing interface
```

By doing so, the system will generate a new graph that includes the new $L_{max}$ based on the newly defined parameters. Also, the system provides the value of $L_{max}$  at the bottom as shown in the screenshot {numref}`li2005_10` . 

```{figure} images/Liedl10.png
---
scale: 90%
align: center
name: li2005_10
---
Output of single computing interface of CAST
```

User can also use _sliders_ for changing the values of  **`Thickness`** and **`Dispersivity`** that appear below the **`Maximum Plume Length`**,as shown in the above screenshot {numref}`li2005_10`, to see how the Plume Length changes upon changing these parameters. 

The sliders will only appear after the first computation is made, i.e., {numref}`li2005_9` is complete.

In case you wish to see the graph on _Fullscreen_ mode, please click on the button **`view full screen graph`**.

```{figure} images/Liedl11.png
---
scale: 90%
align: center
name: li2005_11
---
Observing out in full-screen 
```

```{figure} images/Liedl12.png
---
scale: 90%
align: center
name: li2005_12
---
Full-screen view of CAST result 
```

Moving your cursor to the top right corner of the graph to reveal the advanced options bar. These options enable you to download/export and explore the graph more precisely. This will provide the options observed in the screenshot {numref}`li2005_11`



```{figure} images/Liedl13.png
---
scale: 90%
align: center
name: li2005_13
---
Observing out in full-screen 
```

To download the graph as a **.png** file, please click on the option represented by the _camera_ icon.

```{figure} images/Liedl14.png
---
scale: 90%
align: center
name: li2005_14
---
Downloading the output graphics
```

The output graphics of CAST is interactive and several options are available for user interactivity with results and database. The available options are:
`Zoom`, `Pan`,`Box Select`, `Lasso Select`, `Zoom in_ and _Zoom out`, `Auto scale`, `Reset Axes`, `Toggle spike lines`, `Show closest data on hover`, and `Compare data on hover`.

### Using Multiple Computing Simulation for Liedl et al. (2005) model ###

**`Multiple computing mode`** is suitable for _scenario based modeling._ In this one can create several scenarios by changing model input parameters and obtain $L_{max}$ for all scenarios at ones. This helps comparing between different created scenarios.    

Now, in case a user wants to use the **`Multiple Computing Simulation`**, one need to click on the option, located in top bar, as seen in {numref}`li2005_15`.

```{figure} images/Liedl15.png
---
scale: 90%
align: center
name: li2005_15
---
Selecting Multiple Computing Simulation option
```

By doing so, you will be directed to this screen where you can select/upload multiple sites for your analysis. 
You can select sites from the already existing _dataset_ for which please click on **`All sites button`**, as shown. Upon clicking, a dropdown will appear which contains a list of sites. To select the sites, please select the **`checkboxes`** adjacent to the site names, as shown on screen. 

Image Liedl 16 and 17..

```{figure} images/Liedl16.png
---
scale: 90%
align: center
name: li2005_16
---
Selecting data from CAST main dataset for comparision with user data I
```

```{figure} images/Liedl17.png
---
scale: 90%
align: center
name: li2005_17
---
Selecting data from CAST main dataset for comparision with user data II
```


You can also _upload_ your own site dataset for which you have to first download _the data template_ file (a _.csv_ file). For this first you need to download the sample by clicking at **`Download Sample File`** (see {numref}`li2005_18a`).  Please download the _.csv_ file and fill your data as you wish. The filling of data or creating of scenario can be done while being _offline._

```{warning}
Do not change the heading name used in sample file.
```
Once your data _.csv_ is ready, click on **`Choose File`** option, a search and select window will appear from where you can select your required file and finally click on **open** button to select it. The screenshots below shows the actions

Image Liedl 18 and 19..

```{figure} images/Liedl18.png
---
scale: 90%
align: center
name: li2005_18
---
Sample file upload I
```

```{figure} images/Liedl19.png
---
scale: 90%
align: center
name: li2005_19
---
Sample file upload II
```

After you have selected you file, _the file name_ will appear next to **`Choose File`** button. Next, please click on **`Upload`** button as shown on {numref}`li2005_20`, and based on the parameters defined in your file, system will generate the $L_{max}$ results on screen.  

```{figure} images/Liedl20.png
---
scale: 90%
align: center
name: li2005_20
---
Uploading user created scenario (.csv) file in the CAST multiple computation interface
```

The user needs to make sure that the file is in the format of the sample dataset. In such cases and in the case where the range or values of parameters don’t match the permitted, system will display an error message (see {numref}`li2005_21`). You are requested to rectify all the issues before uploading again.

```{attention} 
The online version of CAST has restricted parameter range. This is required to ensure that calculation and results are displayed with available internet requirements

For the offline version, the range can be set by user themselves.
```

```{figure} images/Liedl21.png
---
scale: 90%
align: center
name: li2005_21
---
Uploading user created scenario (.csv) file in the CAST multiple computation interface
```

In case you want to add data _manually_ here only, then please click on the **`Add Data`** button as shown on screenshot {numref}`li2005_22`). This option is good if user only intends to create only few scenarios. 

```{figure} images/Liedl22.png
---
scale: 90%
align: center
name: li2005_22
---
Manually adding scenario data to CAST
```

By doing so, new window will appear on screen, here you can enter you data manually into the system and after entering the data in all the fields, please click on the **`Generate Graph`** button.

Image Liedl 23..

```{figure} images/Liedl23.png
---
scale: 90%
align: center
name: li2005_23
---
Manually adding scenario obtaining the results
```

If the entered values are in permitted range, system will display a message, **your entry has been added**. And based on the parameters defined, system will generate a new graph- see the screenshots {numref}`li2005_24a`) and {numref}`li2005_24b`)

```{figure} images/Liedl24a.png
---
scale: 90%
align: center
name: li2005_24a
---
Generated results for scenarios I
```

```{figure} images/Liedl24b.png
---
scale: 90%
align: center
name: li2005_24b
---
Generated results for scenarios II
```

In case you wish to **delete** your results and start from fresh, please click on **`delete table data`* button, as shown in {numref}`li2005_25`) and {numref}`li2005_26`)

```{figure} images/Liedl25.png
---
scale: 90%
align: center
name: li2005_25
---
Manipulating scenario data I
```

```{figure} images/Liedl26.png
---
scale: 90%
align: center
name: li2005_26
---
Manipulating scenario data II
```

The results obtained can be download in three different formats, `.csv`, `.xls`, and `.pdf`. 

```{figure} images/Liedl27.png
---
scale: 90%
align: center
name: li2005_27
---
Downloading/saving obtained results in different formats
```

In case you want to print out of your results, please click on the **`print`** button, as shown on attached screenshot.

Image Liedl 28 and 29..

```{figure} images/Liedl28.png
---
scale: 90%
align: center
name: li2005_28
---
Printing the obtained results I
```

```{figure} images/Liedl29.png
---
scale: 90%
align: center
name: li2005_29
---
Printing the obtained results II
```






