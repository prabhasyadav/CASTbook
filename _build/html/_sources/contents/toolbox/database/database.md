### CAST Toolbox - Site Database and Data Visualization

#### Site Database ###

Site Database helps to view the data of the site along with various parameters of the site and those required by the models. Two types of site data are available within the CAST. 

1. {ref}`Unmodifiable site data<unmod_data>` 
2. {ref}`Additional user data<user_data>`

(unmod_data)=  
#####  Unmodifiable site data ######

These are data from the literature (see the screenshot below) and thus considered the _standard dataset_. This dataset is used for comparing model results. The user can download this dataset as a **.csv** file.

```{figure} images/db_f1.png
---
scale: 60%
align: center
name: db1
---
Standard site dataset of CAST
```

The standard dataset can be **searched** for any specific name or data value within data. The parameters that are included in the _database_ are: `Site name`, `Compound`, `Aquifer Thickness` `Plume length`, `Plume Width`, `Hydraulic Conductivity`, `Electron Donor (Contaminant Concentration)`, `Oxygen`, `Nitrate`, `Sulphur Oxide`,`Ferrous`, `Plume State`, `Chemical Group`, `Country`, and `Literature Source`

Plume state in the database refers to the site condition, e.g, steady-state. This is a very important information because the maximum extents of contamination is observed at the steady-state. Models provided in CAST actually provides the maximum length of the plume, i.e., $L_{max}$.


##### Dispersitivity dataset  #####

**Dispersivity** is among the most critical quantity required for obtaining plume extensions. However, dispersivity data are almost never available (see {numref}`db1`), and diligent estimate of it needs to be made for using in models. More critical are transverse dispersivity data, mostly because of their very low magnitude. Due to this reason, **CAST** includes a dataset of dispersivity (see {numref}`db3`) found in the literature. 


```{figure} images/db_f3.png
---
scale: 60%
align: center
name: db3
---
Transverse dispersivity dataset in CAST
```

**Dispersivity** dataset in CAST is an isolated dataset. It is only provided for reference purpose such that user can make an appropriate estimate when using models. To facilitate further, the exploratory data analysis of  dispersivity dataset is provided (see screenshot {numref}`db4` ).

```{figure} images/db_f4.png
---
scale: 60%
align: center
name: db4
---
Analysis of transverse dispersivity dataset
```

(user_data)=
##### User data #####

**Additional user data** let users add their own data and compare them with the _standard dataset_. User can add data directly to the table by clicking `Add data` button (see screenshot {numref}`db2` ), clicking of which opens a data input windows. This option can be tedious if many site data are to be included as the _user data._ 

User can also add their data using the `Download sample file` (see screenshot {numref}`db2`) button. This will download a sample data input (**.csv**) file to the user's computer. The sample file can be filled with data, and then uploaded to the CAST using the `upload` button. Users are not required to be **online** while working of the sample file. 

```{attention} 
The **heading** used in the sample file should not be changed. Also, the file format for upload should be a **.csv** file.

**Error** message will be displayed when the sample file format or heading is changed.
```

```{figure} images/db_f2.png
---
scale: 60%
align: center
name: db2
---
User data input interface in CAST
```

**User data** can be saved in different formats such as **csv**, **xls**, **pdf** or printed. 

```{warning} 
The `delete table data` button will delete the entire user data in the table. Users should save their data before using this button.

Deletion of selective data row is still not implemented in CAST.

```

#### Data Analysis and Visualization ####

**CAST** provides only a limited data analysis and visualization options. However, the provided options are certainly good enough to have an impression of site data including user data. Users are provided options for downloading data in _editable_ format (e.g., csv) through **CAST** interface (see {numref}`db1` ). This simplifies users data analysis outside of **CAST**. 

```{note}
**CAST** data analysis allows user to compare the {ref}`unmod_data` and {ref}`user_data`
```

##### Accessing Visualization and Data Analysis Interface of CAST ##### 

Under the heading of **Analysis Visualisation**, the dropdown menu provides the visualisation options of CAST (see screenshot {numref}`db5`). Data summary table is also part of the analysis. The ``All Plots`` option gives the user an overview of all the plots and _clicking_ them individually gives the information on the clicked plot type. Different plot-types and options available with them are discussed below. Open-source data visualization library [Plotly](https://plotly.com/python/) is used for plots and visualization in **CAST**. 

```{figure} images/db_f5.png 
---
scale: 50%
align: center
name: db5
---
Visualization options of CAST
```

##### Bargraph 

The Bargraph shows the _Plume Length_($y$-axis) versus the _Site Number_ ($x$-axis). The _Site Number_ are randomized order of site found in the database table. There are several features within each of the plot-types, which can be used interactively. These options provide very useful way to understand data. These options included ``Download as png``, ``Zoom``, ``Pan``, ``Box Select``, ``Zoom in``, ``Zoom out``. Furthermore, there is also a option to provide the graph in a _fullscreen mode_. This let user interact with visuals more appropriately.

```{figure} images/db_f6.png 
---
scale: 60%
align: center
name: db6
---
Bargraph of the plume length
```

##### Boxplots

Boxplot is the other plot-type that can be used to visualize site datasets in CAST. In this plot, users can observe the _mean_, _median_, _maximum_ and _minimum_ values for FOUR different site parameters: ``PLume Length`` (see screenshot {numref}`db_f7`), ``Aquifer Thickness``, ``Electron Donor``, ``Electron Acceptor`` in the plot. Note that ``Electron Donor`` refers to _Contaminant Concentration_ and ``Electron Acceptor`` the partner reactant such as Oxygen, Nitrates etc. User can interact using the  features (zoom, box select etc., {numref}`db_f6`) 

```{figure} images/db_f7.png 
---
scale: 50%
align: center
name: db7
---
Boxplots of several site quantities.
```


##### Histograms and Distributions 

Histogram plots of CAST also attempts to provide limited types of _continuous distributions_ of the data. By default, the histogram shows the _Guassian_ distribution for ``Plume Length`` data, which can be changed to _Lognormal_ and _Exponential_ distributions. Distribution and fits are provided also for other site parameters  ``Electron Donor``, ``Electron Acceptor`` and ``Aquifer Thickness``. The screenshot from CAST (below) provides a clearer picture of the available options of Histogram plot-type from CAST.

```{figure} images/db_f8.png 
---
scale: 70%
align: center
name: db8
---
Histogram and underlying distribution type of site parameters.
```
The distribution fitting of the Histogram in CAST is performed using the open-source Scipy library [scipy.stats](https://docs.scipy.org/doc/scipy/reference/stats.html). The code snippets (from CAST below) shows the implementation of Python code for the distribution fits. The complete codes are available [here](https://github.com/CAST-IIT/CAST/blob/Personal-CAST-development/groundwater/databasePlots.py)

```python
def create_histogram(histogramFeature, table_data, index, parameter):
    plume_data = df[parameter]
    if parameter == "Electron Donor[mg/l]":
        plume_data = [int(x) for x in plume_data]
    plume_data = [x for x in plume_data if str(x) != 'nan']

    mu, std = norm.fit(plume_data)
    x = np.linspace(0, max(plume_data))
    # Get current size
    fig_size = plt.rcParams["figure.figsize"]
    fig_size[0] = 10  # width
    fig_size[1] = 5
    plt.rcParams["figure.figsize"] = fig_size
    plt.hist(plume_data, density=True, color='#ffa600', alpha=0.7)
    if histogramFeature == 'Gaussian':
        y_pdf = ss.norm.pdf(x, mu, std)
        plt.plot(x, y_pdf, color='#d45087', linewidth=3)
    elif histogramFeature == 'Log Normal':
        y_log = ss.lognorm.pdf(x, mu, std)
        plt.plot(x, y_log, color='#a05195', linewidth=3)
```


##### Scattered Plots

Scatter Plots provide an option to compare among a pair of site parameters. This plot-type in addition to visualization also aid in quantifying correlation and underlying fit between parameters. The screenshot below shows options available within the Scatter plot interface of CAST. Plot provides interactive options such as ``zoom``, ``pan`` etc as discussed above.


```{figure} images/db_f9.png 
---
scale: 70%
align: center
name: db9
---
Scatter plots and fit options in CAST.
```

Scatter plots are fundamental in developing models. Therefore, in CAST in addition to the visualization, different fit-types: ``Exponential``, ``Linear``, ``Power 2``, ``Power 3``) are provided between different site parameters (e.g., ``Aquifer Thickness``, ``Electron Donor``) with the ``Plume Length`` (see {numref}`db9`). Plume Length in CAST is the main output quantity. The main output of the Models used in CAST (see [](../an_model/an_model.md)) is maximum plume length or $L_{max}$.

Data fits in CAST is performed using the open-source Scipy library [scipy.optimize](https://docs.scipy.org/doc/scipy/reference/optimize.html). In particular the function provided by ``curve_fit`` in scipy.optimize is used for the fitting. Fit parameters including $R^2$ value are currently not provided as intention in the current version of CAST data-analysis is to only present the first-hand information of data. Users are provided option to _download_ data in editable format, which simplifies full-scale data analysis. The code snippet below shows the **fit** implemented in CAST. Complete code can be obtained from [here](https://github.com/CAST-IIT/CAST/blob/Personal-CAST-development/groundwater/scatterplot.py).

```python
    if feature == 'Exponential':
        # for exponential fit
        popt, pcov = curve_fit(exponenial_func, merged_list, y, p0=(1, 1e-6, 1), maxfev=5000)
        xx = np.linspace(1, len(merged_list), len(merged_list))
        yy = exponenial_func(xx, *popt)
```

#### Statistical Description of Data 

This provide a statistical (numbers) overview of the data.  Statistical quantities such as ``mean``, ``median``, ``standard deviation`` among others provide a good insight of the data, and simplifies comparison between large site data and other usually (small) user site data. The screenshot below shows the CAST output of the site description.

```{figure} images/db_f10.png 
---
scale: 50%
align: center
name: db10
---
Stastiscal overview of the site data
```
