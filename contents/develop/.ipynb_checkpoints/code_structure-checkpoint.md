## CAST Code Structure 


```{figure} images/CS_f1.png
---
figclass: margin-caption
figclass: margin
scale: 60%
align: center
name: CS1
---
The main code structure of CAST
```

The structuring of CAST is as follows :

* `groundwater` : The main coding folder 
* `create_database.py` : Python file for creating/updating database 
* `run.py` : Python file for running CAST
* `mf2005, mf2005.exe,mt3dms,mt3dms.exe` : Executable files used by the numerical mode
* `requirements.txt` : Python packages/libraries used in the project

Other files include _readme_, _licensing_, _installation_ files etc.
{numref}`CS1` shows the screenshot of the main code structure of CAST.



The struction of the main coding folder `groundwater` is as follows :

* `static` : Cascading Style Sheets, images, fonts, comma separated value files and JavaScript codes
* `templates` : HTML codes
* `NumericalModel` : Code for the numerical model


```{figure} images/CS_f2.png
---
figclass: margin-caption
figclass: margin
scale: 60%
align: center
name: CS2
---
The main code structure of CAST
```


Other files include python files consisting of routes, initialisation and integration codes for CAST.
{numref}`CS2` shows the screenshot of the code structure of the `groundwater` folder of the CAST.
