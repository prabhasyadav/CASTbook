## CAST Code Libraries 

### Python ###
[Python](www.python.org) is an OSI-approved open source license programming language. The version of Python used for CAST is **3.6.8**.

### Flask Framework ###
[Flask](https://palletsprojects.com/p/flask/) is a micro web framework written in Python. It is classified as a micro-framework because mostly does not require particular tools or libraries. It is open/modular, allowing developers to use their preferred packages and dependencies. It supports extensions that can add application features as if they were implemented in Flask itself. It helps the project by integrating the dataset, the visualisations, all the Python libraries and interfacing.

*	Flask is open source, highly extensible, easily integratable and OS independent.
*	Flask has been developed by Armin Ronacher and has been licensed under BSD.

It is based on WSGI toolkit and [jinja2](https://palletsprojects.com/p/jinja/) template engine. WSGI is an acronym for **W**eb **S**erver **G**ateway **I**nterface which is a standard for python web application development. Jinja2 is a web template engine which combines a template with a certain data source to render the dynamic web pages. For CAST, the stable version **1.0.2** of Flask is used.


```{figure} images/CS_f3.png
---
scale: 60%
align: center
name: CS3
---
The [Flask](https://palletsprojects.com/p/flask/) framework of CAST
```
{numref}`CS3` above shows how the Flask framework functions

### Front End Libraries ###

#### HTML ####
According to the MDN Web Docs, [HTML](https://html.spec.whatwg.org/) (**H**yper**T**ext **M**arkup **L**anguage) is the most basic building block of the Web. It defines the meaning and structure of web content. Other technologies besides HTML are generally used to describe a web page's appearance/presentation ([CSS](https://www.w3.org/TR/CSS/#css)) or functionality/behavior ([JavaScript](https://en.wikipedia.org/wiki/JavaScript)). CAST uses HTML5 i.e., the fifth revision of HTML.

#### CSS ####
The World Wide Web Consortium defines [CSS](https://www.w3.org/TR/CSS/#css) (**C**ascading **S**tyle **S**heets) as a simple mechanism for adding style (e.g., fonts, colors, spacing) to Web documents.

#### BootStrap ####
[Bootstrap](https://getbootstrap.com/) is an HTML, CSS, and JavaScript framework for developing responsive websites. It is free as well as open-source.

#### JavaScript ####
[JavaScript](https://en.wikipedia.org/wiki/JavaScript) is a lightweight, interpreted, object-oriented language with first-class functions, and is best known as the scripting language for Web pages, and is used in many non-browser environments as well. It is a prototype-based, multi-paradigm scripting language that is dynamic, and supports object-oriented, imperative, and functional programming styles.

### Python Libraries ###

#### Pandas ####
[Pandas](https://pandas.pydata.org/) is an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools. Pandas data frames is generally used for representing Excel<sup>TM</sup> Like Data In-Memory.

#### NumPy ####
[NumPy](https://numpy.org/) adds support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.

#### SciPy ####
[SciPy](https://www.scipy.org/) is a collection of mathematical algorithms and convenience functions built on the NumPy extension of Python. It adds significant power to the interactive Python session by providing the user with high-level commands and classes for manipulating and visualizing data. With SciPy an interactive Python session becomes a data-processing and system-prototyping environment rivalling systems such as MATLAB<sup>TM</sup>, Octave, R-Lab, SciLab.

```{figure} images/CS_f4.png
---
scale: 60%
align: center
name: CS4
---
Code snapshot showing usage of Python libraries in CAST
```

{numref}`CS4` above is a snapshot of a code from CAST displaying various Python libraries like _Numpy_, _SciPy_, _Matplotlib,_ and _Plotly_ . This code is helping to make a scatterplot visualisation with fits (linear, exponential etc)



#### FloPy ####
[FloPy](https://www.usgs.gov/software/flopy-python-package-creating-running-and-post-processing-modflow-based-models) is a Python package to create, run, and post-process MODFLOW-based models. CAST uses _FloPy_ for running the numerical model.

```{figure} images/CS_f5.png
---
scale: 60%
align: center
name: CS5
---
FloPy code used in CAST
```

{numref}`CS5` above is a snapshot of a code from CAST displaying how FloPy is being used for the numerical model

#### Matplotlib ####
[Matplotlib](https://matplotlib.org/) is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms. Matplotlib can be used in Python scripts, the Python and IPython shells, the Jupyter notebook, web application servers, and four graphical user interface toolkits.

#### Plotly ####
[Plotly](https://plotly.com/) provides online graphing, analytics, and statistics tools for individuals and collaboration, as well as scientific graphing libraries. It allows you to make beautiful, interactive, exportable figures in just a few lines of code. It uses D3.js behind the scenes and has API wrappers for R, Julia, and many other languages.

#### SQLAlchemy ####
[SQLAlchemy](https://www.sqlalchemy.org/) is the Python SQL toolkit and Object Relational Mapper that gives a flexibility for SQL. It provides a full suite of well known enterprise-level persistence patterns, designed for efficient and high-performing database access, adapted into a simple and Pythonic domain language.

### Backend ###

#### MySQL ####
[MySQL](https://www.mysql.com/) is an open sourced RDBMS (**R**elational **D**atabase **M**anagement **S**ystem). CAST uses MySQL to store the data of all models as well as login information of all users. The passwords of all users are stored in an encrypted manner in the database as well.

```{figure} images/CS_f6.png
---
scale: 60%
align: center
name: CS6
---
MySQL use in CAST
```

{numref}`CS6` above is a snapshot of a code from CAST displaying the tables/relational mappings for MySQL

