## **C**ontamination **A**ssessment and **S**ite management **T**ool or **CAST** ##
------------------------

**CAST** is a browser based model applications for the assessment of contaminated sites, specially for BTEX-type contaminations. The most important objective of the **CAST** is to provide an easy interface for exploring sites, such that a preliminary decision on site-assessment can be made. **CAST** at the current stage targets sites that has never been assessed of risks they pose- e.g., [Potentially Contaminated Sites](https://www.eea.europa.eu/data-and-maps/indicators/progress-in-management-of-contaminated-sites-3/assessment).   

The specific highlight of CAST is the online application accessible from www.cast.iitd.ac.in. The online application restricts the range of input values to ensure that computations are possible also when the internet connectivity are weak. The offline version have no such restrictions. 

### Citation of CAST ###
To be provided later...,

### Open-source code and license terms ### 

The CAST codes are open-sourced and are licensed under Creative Commons CC BY-SA 4.0. Please check [here](https://creativecommons.org/licenses/by-sa/4.0/) for license wordings.  

```{figure} images/intro_images/cc.png
---
scale: 50%
align: left
name: cc
---
```

CAST codes are hosted in Github, and can be obtained from: [here](https://github.com/CAST-IIT/CAST)


### Non-resposibility Declaration ###


**Authors and organizations of CAST can not be held responsible for any results or output obtained from using the website or the codes provided here**

### CAST Code development and Models ###

[Flask](https://palletsprojects.com/p/flask/) micro web-framework is used for the web-application development. The front end of the **CAST** has been designed using HTML, CSS and bootstrap. The back-end is being handled by the open-source management systems: [MySQL](https://www.mysql.com/) and [Python(3.6.8)](https://www.python.org/downloads/release/python-368/). 

The CAST code structure can be visualized from the following flowchart:

```{figure} images/intro_images/Overview_CAST.png
---
scale: 100%
align: center
name: flowchart
---
The CAST flowchart
```

**CAST** is a work under progress, as such not all its components, called **Toolboxes** are already implemented. Furthermore, the models within the toolbox or the applicable function and interactivity are currently quite limited. However, as is also described below, the current state of CAST can already be considered as a useful application. The toolboxes of CAST can be seen in the following figure.


```{figure} images/intro_images/MainPage.png
---
scale: 30%
align: center
name: cc
---
The main page of CAST
```

The **Toolboxes** of CAST provides the applicable functionalities. Each toolbox and the available functions are detailed in successive chapters of this documentation. Here a very brief overview of the CAST toolboxes is presented.


#### Data toolbox ####

+ Large contaminated site database (100+ sites)
+ Statistical measures and visualizations of important site quantities

```{figure} images/intro_images/AllPlotsDb.png
---
scale: 30%
align: center
name: Database toolbox
---
The plots from Database toolbox
```

#### Analytical models toolbox ####

The toolbox currently contains 5 analytical models including the widely used version of BIOSCREEN model called BIOSCREEN-AT. The included models (see model chapter **XXYY**) for more details individually) in the current version of **CAST** are:

+ 2D Vertical Model (Liedl et al., 2005)
+ 2D Horizontal Model (Ham et al. 2005, Chu et al., 2005)
+ 3D Model (Liedl et al., 2011)
+ 3D Model (BIOSCREEN-AT, Karanovic et al., 2007)


```{figure} images/intro_images/AnalyticalModels.png
---
scale: 40%
align: center
name: An_mod
---
Analytical models in analytical model toolbox
```

#### Empirical models for toolbox ####

There are only limited Empirical models available. The **CAST** empirical toolbox contains the following models (see model chapter **XXYY** for details): 

+ 2D Vertical (Maier and Grathwohl, 2005)
+ 2D Vertical with richarge (Birla et al. 2020)

```{figure} images/intro_images/em_model.png
---
scale: 40%
align: center
name: em_mod
---
Empirical models in empirical model toolbox
```

#### Numerical model toolbox ####

Numerical model is widely used for site assessment. However, this model type is used for more comprehenisve site assessment works. On the other hand, **CAST** focuses on intial assessment of sites. Therefore, a very simple numerical model based on  [MODFLOW](http://tiny.cc/kon6jz) and [MT3D-MS](http://tiny.cc/6pn6jz) with very limited function is part of the CAST. More details of the numerical model is provided in Chapter **XXXXXX**.

```{figure} images/intro_images/NumericalModel.png
---
scale: 40%
align: center
name: An_mod
---
Numerical model in numerical model toolbox
```

#### Decision model for selection of model for site-assessment ####

This toolbox is not still implemented in **CAST**.

### Online deployment of CAST ###

* The online application of CAST (www.cast.iitd.ac.in) has its storage on <a href="https://baadal.iitd.ac.in/baadal">Baadal</a>, which is a cloud orchestration and virtualization management software developed at Indian Institute of Technology Delhi (IITD).

* It has been deployed on an Ubuntu 16.04 server with 2 CPU, 4GB RAM and 80GB HDD. 


### The development organization and members ###

**CAST** has received support from researchers and facilities of Indian Institute of Technology Delhi (IITD), Dresden University of Technology (TUD), Manipal University Jaipur (MUJ), and University of Texas at Austin (UT-Austin). 

```{figure} images/intro_images/alluni.png
---
scale: 60%
align: center
name: all_uni
---

```

The XXXX chapter provide complete details of the developers, researchers and organizations invovled with the **CAST**.

**Funds** for the **CAST** development were obtained from:

1. Partially through DFG fund (LI 727/29-1)   

```{figure} images/intro_images/DFG.png
---
scale: 40%
align: left
name: DFG
---

```

2. Funding through:</br>
     1. Professional Development Fund of Prof B R Chahar</br>
     2. Ministry of Water Resources, Govt of India



