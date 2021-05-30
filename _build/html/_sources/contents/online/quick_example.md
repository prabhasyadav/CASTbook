## Quick usage example of CAST ##


### 1. Using Analytical model in CAST ###

#### Using Single Computing Simulation ####

Clicking the **Analytical Toolbox** box in the homepage will lead to the interface that lists  all the analytical models available in the CAST. From here choose the  model that you wish to use. As an example here -  _Liedl et al.(2005)_ has been used. For using Liedl et al. (2005), from the interface shown in the screenshot below, please click on the option **`Click here to see the model`** below the Liedl et al. (2005) as shown in the  screenshot below. 

Please click on option Liedl et al. (2005), located in the _top_ bar, to open the dropdown menu containing the two options for computation. In case a user wishes to model a single site (as is the case in the example) or a number of sites but one at a time **`Single computing simulation`** option can be used. 

After clicking on **`single computing simulation`**, you will be directed towards the below attached window. The area highlighted in red square contains the _input_ parameters for the model where the user needs to enter the required values in the fields . Then please click on the **`Generate Graph`** option as shown on screen and the user can see the value of **`Maximum Plume Length`** as shown in the screenshot. 

```{figure} images/on3.png
---
scale: 70%
align: center
name: quickeg1
---
The quick way to use the **single computing interface** in CAST
```


The obtained results can be interacted using sliders and the options available in the graph. For details check the documentation of each models provided [here](../../contents/toolbox/an_model/an_model.md)

#### Using Multiple Computing Simulation ####

The **`multiple computing simulation`** mode of CAST let user create multiple sceanrios and compare them with field data of their choice. Once the user is in their choice of analytical model, they slect **`multiple computing simulation`** in the dropdown menu from the _top_ bar. This opens the interface for **`multiple computing simulation`**. 

In the interface user need to create scenario. This can be done by filling dataset one at a time or more elegantly by downloading the template csv file and then uploading it back. This way user can input several data all at once.

Once data are uploaded the data table gets filled and the model results are generated in the plot. User can choose the site of their choice to compare their scenario. More details on these steps can be obtained from [here](../../contents/toolbox/an_model/an_model.md). The screenshot below clarifies the steps. 

```{figure} images/on4.png
---
scale: 70%
align: center
name: quickeg2
---
The quick way to use the **multiple computing interface** in CAST
```

### 2. Using Empirical model in CAST

Clicking the **Empirical Toolbox** box in the homepage will lead to the interface that lists  all the analytical models available in the CAST. From here choose the  model that you wish to use. As an example, Maier And Grathwohl (2006)has been used. For using Maier And Grathwohl (2006), from the interface shown in the screenshot below, please click on the option **`Click here to see the model`** below. 

The process thereafter is exactly similar to that discussed for the analytical model. Empirical models are described [](../../contents/toolbox/em_model/em_model.md)


### 3.Using Numerical model in CAST

Numerical model in CAST is based of MODFLOW/MT3DMS. Complete detail of the model is provided [here](../../contents/toolbox/num_model.md)

For working with the numerical model, click on the **Numerical Toolbox** box in the homepage. Please click on option **Numerical Model**, located in the _top_ bar, to open the dropdown menu as shown in the screenshot and click on the **`single computing simulation`** from there. Enter the required values in the fields and then please click on the **`Run`** option to get the **`Maximum Plume Length`**. The screenshot below presents the steps. Pls note that simulation can take time depending on the input data. 

```{figure} images/on5.png
---
scale: 50%
align: center
name: quickeg3
---
The quick way to use the **Numerical computing interface** in CAST
```