### Using CAST OFFLINE ###

CAST is not necessary an ONLINE tool. It is essentially a browser-based tool, which can be used in both ONLINE and OFFLINE. However, for the OFFLINE use, **CAST** has to be installed in the local system. The OFFLINE set-up of CAST is provided below in detail.

```{tip}
**The OFFLINE use of CAST is recommended, as parameter range limits used in ONLINE mode can be avoided**.
```


#### Installation of Softwares required for successful running of CAST ####
The **offline** installation of CAST depends on _carefully_ following the steps that require few (open-source) software to be installed, and various system changes at the OS level to be made. The installation process is presented in steps below with outcomes (of each step) with the help of pictures. A careful read of the steps presented below before installing CAST can be very useful for the installation and offline use of the CAST. 

```{attention}
**The step presented below are for Windows<sup>TM</sup> OS**.
```

**CAST** can be installed in any OS. The intallation steps required for other OS (Linux/MacOS<sup>TM</sup>) will be documented later.

#### Step 1. Installation of the Github Desktop ####

Installation of [**Github Desktop**](https://desktop.github.com/) is **recommended** as it simplifies the _first_ installation process, specially for new users. Besides Github Desktop also simplifies any personalized modification of **CAST** code and updates.

 [Click to visit **Github Desktop**](https://desktop.github.com/) and follow the installation process. The screenshot below shows the interface of **Github Desktop** website.

```{figure} images/off_f1.png
---
scale: 40%
align: center
name: of1
---
The [**Github Desktop**](https://desktop.github.com/) set-up
```

After the successful installation of Github Desktop, ``open`` the Github Desktop Application and click on ``clone a repository``. Under URL, paste the URL ``https://github.com/CAST-IIT.git`` as seen in the screenshot below. This can also be alternately seen under CAST-IIT/CAST at Personal-CAST-development github.com, under ``Code``.

```{note}
**Personal CAST** is the default branch/master branch and for OFFLINE use. **Professional branch** is used for the ONLINE **CAST**. 
```

```{figure} images/off_f2.png
---
scale: 50%
align: center
name: of2
---
Cloning CAST source repository from Github
```

The _cloning_ of the **CAST** will begin in your computer. You can store the cloned to your desired directory in your computer.

#### Step 2. Installation of Python system in the local computer ####

**Step 2A.** Downloading appropriate Python version : 

From the website ‘ https://www.python.org/downloads/ ’, download version 3.6.8 of Python (see steps in the screenshot below). You should choose 64 bit version. 

```{figure} images/off_f3.png
---
scale: 50%
align: center
name: of3
---
Downloading Python version 3.6.8
```

```{warning}
Python version 3.6.8 is **required**.  
```
**Step 2B.** Installation of Python and adding its ``path`` to the system 

Open the Python executable ``.exe`` file that you downloaded Do not forget to check the box that says **Add Python 3.6 to Path**. Then, click on ``Install Now`` button (see the screenshot below).

```{figure} images/off_f4.png
---
scale: 50%
align: center
name: of4
---
Installing Python and adding Python path.
```
 
**Step 2C.** Installation of ``pip``
``pip`` is Python package (library) management system. After completion of Python setup, it is a mandatory step to check if ``pip`` is also installed and for the required version of the Python, for that we go to the ``Command Prompt`` and type ``pip --version``. When pip is instlled, it's version will be the output (see screenshot) 
   
```{figure} images/off_f5.png
---
scale: 70%
align: center
name: of5
---
Checking installed pip version
```
**Step 2D.** Installation of ``pip`` when not installed
In case **no** pip version is found, we can install it through command prompt by entering the command- ``python get-pip.py``. Once installed it is a good idea to re-check the installed pip. Re-checking can be done using ``pip --version`` as above. Additionally, to verify the version of python, we can see it through the  line of command ``python --version``



**Step 2E.** Installation of **Virtual Environment (VE)**: <br>

A [Virtual Environment](https://docs.python.org/3/library/venv.html) (VE) is a _tool_ or a _folder_ that helps to keep dependencies required by different Python projects separate. CAST is a Python project, as such we create a separate Python system (a VE) for CAST. This can be easily done using command prompt (see screenshot below) and entering the command ``pip install virualenv``. 

```{note}
``virtualenv`` is an independent Python [library](https://virtualenv.pypa.io/en/latest/) and it can be installed out of CAST directory. 
```

```{figure} images/off_f6.png
---
scale: 70%
align: center
name: of6
---
Installing Python Virtual Environment
```
**Step 2F.** Setting-up Virtual Environment (VE) for the **CAST** project

```{caution}
Make sure you are in the **CAST** directory-
```

- Create Virtual Environment files:
Make sure you are in the **CAST** directory- the directory where you stored the _cloned_ CAST repository (see **Step 1**). Look at the below screenshot:

```{figure} images/off_f7.png
---
scale: 70%
align: center
name: of7
---
Creating VE called venv for the CAST project.
```

- Activation of VE venv:

```{caution}
Make sure you are in the **CAST\venv\Scripts** directory-
```
 The created VE venv has to be activated before it can used. This can be done using the command ``activate`` in the ``venv\Scripts`` directory of CAST (see screenshot below). Once activated, you will see the ``<venv>`` at the start of the prompt (see screenshot) 

```{figure} images/off_f8.png
---
scale: 70%
align: center
name: of8
---
Ativating Virtual Environment
```
#### Step 3. Installing Python libraries required by the **CAST** project ####
With VE created and activated, it is now time to install the Python libraries that are used in CAST. The required libraries are listed in the **.txt** file called ``requirements.txt``. There are several libraries to be installed, e.g., Numpy, Scipy, Matplotlib. Depending on your (internet) connection speed it may take up to 30 minutes (typically for High-speed connection) for installing all the required libraries.

The installing is easy a single _pip_ command ``pip install -r requirements.txt`` will get it all done (as in the screenshot below). 

```{attention} 
- The ``pip install -r requirements.txt`` command must be used in the **CAST** directory.
- Do **not** close the the command prompt after all requirements.txt operation is complete.
```

#### Step 4.	Setting up MySql ####

[MySql](https://www.mysql.com/) is an _open-source_ relational database management system (RDBMS). In **CAST** database is used for managing user account such that user can save their input and output data. For **ONLINE** CAST this means users can retrieve their input at later time. For **OFFLINE** CAST the same structure can be used in the environment when there are multiple people using CAST. User account creation is detailed [here](../online/login.md).

Below step-wise setting up of Mysql is provided. 

- Visit the _webpage_ to download the Mysql installer file [http://dev.mysql.com/downloads/installer/](http://dev.mysql.com/downloads/installer/)  
  
- In the _webpage_, download the file that is about 400 MB (**the offline version**) in size and start the setup. 
  
- Choosing a Setup type: Chose **FULL** (see screenshot)  

```{figure} images/off_f9.png
---
scale: 70%
align: center
name: of9
---
Selecting MySql set-up type
```

- Keep on selecting _default_ set-up by clicking **next**  or **execute**. Please do not skip any steps though.  Different components of MySql will be installed during the process. The screenshot below shows the steps. 


```{figure} images/off_f10.png
---
scale: 40%
align: center
name: of10
---
MySql components.
```

- Keep the **default** set-up option as is it and continue until the ``account setting`` screen is obtained (see screenshot below). Set your **password** and make sure to **remember** this password as in the next few steps, during application of configuration, we can check for the password if it is correct or not.  Not to worry if the password is a _weak_ (although try to use a strong) one.

```{figure} images/off_f11.png
---
scale: 50%
align: center
name: of11
---
Setting MySql root password
```
```{admonition} Kanishk Pls. check
:class : warning
**Do you remember how much time it takes here. I think in one of the step it takes 20-30 minutes. We need to mention that.**
```


- A window **Connect to Server** (see screenshot below) will appear. In this window, _insert_ the **password** that you created in the previous step  and _click_ on the ``check`` button.

```{caution}
Make sure that you do not forget the **password**. The entire MySql set-up have to repeated if you forget the password.
```
   
```{figure} images/off_f12.png
---
scale: 70%
align: center
name: of12
---
Connecting MySql to the local server
```

- After setting  up MySql, open **MySql Workbench** using Windows<sup>TM</sup>  _start-menu_. Click on ``Connections`` and when asked, enter the root ``password`` created during the MySql setup. You should get the windows as shown in the screenshot below
  
```{figure} images/off_f13.png
---
scale: 70%
align: center
name: of13
---
MySql Workbench connection
```

- Create a **database** named ``groundwater`` in the new page. This can be done by writing the command ``create database groundwater`` in the windows space (see screeshot). Once the command is written, **click** on the ``lightning button`` (It is used to execute), and _wait_ until action is shown (see the screenshot) in the bottom. 

```{figure} images/off_f14a.png
---
scale: 70%
align: center
name: of14
---
Creating the ``groundwater`` database
```
```{note}
``groundwater.db`` is the database that CAST centrally uses. When codes are updated, this database has to be updated. 
```
#### Step 5. Executing OFFLINE CAST ####

With creation of the (groundwater) database, setting-up MySql is complete. Next, we move to connect the **OFFLINE CAST** with the local server, the database and the code. These steps are simplified (at least for less CS/IT experts) using specialized text-editor/IDE such as [**Visual Studio Code**](https://code.visualstudio.com/), [**PyCharm<sup>TM</sup>**](https://www.jetbrains.com/pycharm/). In the description we use **Visual Studio Code**. The steps below explains the steps.

- In **Visual Studio Code**, open the ``file`` location; here select **CAST** (the cloned folder in Step 1) and click on ``Open Folder``.

```{figure} images/off_f17.png
---
scale: 70%
align: center
name: of17
---
CAST Code in Visual Studio Code
```

- In the Visual Studio Code on the left-side select the file ``groundwater>config.py``, and change the **password** that was used for setting-up of MySql in **STEP 4** (see screenshot below). 

```{figure} images/off_f18.png
---
scale: 70%
align: center
name: of18
---
Personalizing the OFFLINE CAST code - using root password
```

- Now populate the (groundwater) database with the command  ``python3 create_database.py`` or ``py create_database.py`` in the **command prompt** (**STEP 2**), in which virtual environment ``venv`` is active- as seen in the screenshot below.

```{note}
Make sure you are in the **\CAST** directory and NOT in the **\venv\Scripts** or other directory. 
```

```{figure} images/off_f15a.png
---
scale: 40%
align: center
name: of14
---
Populating the ``groundwater`` database from MySql to CAST
```

- Under ``groundwater/water.py``, change the ``parent_dir= ‘your directory\\CAST``. Note the double-blackslash (\\) used in directory address. This Python programming standard. This is explained in the screenshot below  

```{figure} images/off_f19.png
---
scale: 70%
align: center
name: of19
---
Setting local directory in the CAST code.
```

- The numerical model of **CAST** uses [MODFLOW](https://www.usgs.gov/software/modflow-2005-usgs-three-dimensional-finite-difference-ground-water-model) and [MT3DMS](https://hydro.geo.ua.edu/mt3d/index.htm). The MODFLOW and MT3DMS **.exe** files are called during the numerical model execution. Therefore, the location of **.exe** files in user's computer have to specified in the CAST code system. This has to be done in the CAST file **groundwater/NumericalModel/numericalModel.py** as shown in the screenshot below 

```{figure} images/off_f20.png
---
scale: 70%
align: center
name: of20
---
Setting directory of MODFLOW/MT3DMS **.exe** in the CAST code.
```

- The next step requires that the Python executable used in the developed of CAST that is in virtual environment ``venv``. In **Visual Studio Code** this can be done is the step-wise manner as shown in the screenshots below.


- Click on the interpreter below and select the ``python interpreter -> virtual environment`` that you want to work in 

```{figure} images/off_f21.png
---
scale: 70%
align: center
name: of21
---
Setting the required Python interpreter I.
```
- In case the Python interpreter is not of the **CAST** virtual environment ``venv``, it should be changed. This can be done by clicking on the Python version seen in Visual Studio Code bottom bar. The screenshot below should appear. 

```{figure} images/off_f22.png
---
scale: 70%
align: center
name: of22
---
Setting the required Python interpreter II.
```

- Go to the file  ``run.py`` that is on the left panel of the Visual Code Studio interface, and on the _top right corner_ click on the ``green play button`` to run it. See the screenshot below.  

```{figure} images/off_f23.png
---
scale: 70%
align: center
name: of23
---
Executing CAST.
```

- At the bottom panel (see screenshot) of the Visual Studio Code, a hyperlink will appear when CAST is executed correctly. The hyperlink has to be copied and pasted in a browser to run CAST. 

```{figure} images/off_f24.png
---
scale: 70%
align: center
name: of24
---
Opening CAST in the browser.
```

- The screenshot below should appear once the hyperlink is executed in the browser.

```{figure} images/off_f25.png
---
scale: 70%
align: center
name: of25
---
OFFLINE CAST interface in the browser.
```

- **Optional step** 
```{admonition} Issue with running script in Windows<sup>TM</sup>
:class: error
The Windows<sup>TM</sup> may give the following error:

**Files cannot be loaded because running scripts is disabled on this system. Provide a valid certificate with which to sign the files.**
```
This error can be addressed using the solution provided [here](https://www.beaming.co.uk/knowledge-base/resolved-files-cannot-loaded-running-scripts-disabled-system/) (also see the screenshot). The error is due to default security block of Windows<sup>TM</sup> for running the script.

```{figure} images/off_f16.png
---
scale: 50%
align: center
name: of16
---
Windows<sup>TM</sup> script executing error.
```

You can log in with your email ID and a password. The server can be closed/stopped by clicking ``Ctrl+C`` in the Visual Studio Code.


For re-running the server or using the OFFLINE CAST steps provided in {numref}`of23` and {numref}`of24` has to be executed. 

