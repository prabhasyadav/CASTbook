## CAST Toolbox - Site Database and Model inputs

### Site Database ###

Site Database  helps to view the data of the site along with various parameters of the site and those required by the models. Two types of site data are available within the CAST. 

1. Unmodifiable site data 
2. {ref}`Additional user data<user_data>`
   
**Unmodifiable site data** are data from the literature (see the screenshot below) and thus considered the _standard dataset_. This dataset is used for comparing model results. The user can download this dataset as a **.csv** file.

```{figure} db_f1.png
---
scale: 60%
align: center
name: db1
---
Standard site dataset of CAST
```

The standard dataset can be **searched** for any specific name or data value within data. The parameters that are included in the _database_ are: `Site name`, `Compound`, `Aquifer Thickness` `Plume length`, `Plume Width`, `Hydraulic Conductivity`, `Electron Donor (Contaminant Concentration)`, `Oxygen`, `Nitrate`, `Sulphur Oxide`,`Ferrous`, `Plume State`, `Chemical Group`, `Country`, and `Literature Source`

Plume state in the database refers to the site condition, e.g, steady-state. This is a very important information because the maximum extents of contamination is observed at the steady-state. Models provided in CAST actually provides the maximum length of the plume, i.e., $L_{max}$.


### Dispersitivity dataset  ###

**Dispersivity** is among the most critical quantity required for obtaining plume extensions. However, dispersivity data are almost never available (see {numref}`db1`), and diligent estimate of it needs to be made for using in models. More critical are transverse dispersivity data, mostly because of their very low magnitude. Due to this reason, **CAST** includes a dataset of dispersivity (see {numref}`db3`) found in the literature. 


```{figure} db_f3.png
---
scale: 60%
align: center
name: db3
---
Transverse dispersivity dataset in CAST
```

**Dispersivity** dataset in CAST is an isolated dataset. It is only provided for reference purpose such that user can make an appropriate estimate when using models. To facilitate further, the exploratory data analysis of  dispersivity dataset is provided (see screenshot {numref}`db4` ).

```{figure} db_f4.png
---
scale: 60%
align: center
name: db4
---
Analysis of transverse dispersivity dataset
```

(user_data)=
### User data ###

**Additional user data** let users add their own data and compare them with the _standard dataset_. User can add data directly to the table by clicking `Add data` button (see screenshot {numref}`db2` ), clicking of which opens a data input windows. This option can be tedious if many site data are to be included as the _user data._ 

User can also add their data using the `Download sample file` (see screenshot {numref}`db2`) button. This will download a sample data input (**.csv**) file to the user's computer. The sample file can be filled with data, and then uploaded to the CAST using the `upload` button. Users are not required to be **online** while working of the sample file. 

```{attention} 
The **heading** used in the sample file should not be changed. Also, the file format for upload should be a **.csv** file.

**Error** message will be displayed when the sample file format or heading is changed.
```

```{figure} db_f2.png
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