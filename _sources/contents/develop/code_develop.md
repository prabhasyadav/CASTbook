## CAST Code Development ##

### Offline ###

#### Choosing a framework ####
For the development of CAST, a Python framework had to be chosen. Django and Flask are two of the most popular python frameworks suited for the project. Flask was chosen as because it is flexibile, extensible and light weighted while Django being a heavier framework would not be as much suitable.

#### Virtual Environment ####
In order to keep all projects separate from each other, a virtual environment is a must. For example, Project A requires version 2 of the python library NumPy, however, Project B requires version 3 of NumPy. It would be tedious to upgrade and downgrade the versions while switching between the projects. Hence, to organise and make projects independent of each other, it is important to have virtual environments. 

Pipenv can also be used for the same purpose with a virtual environment inside it. For the development of CAST, a virtual environment is used.

#### Choosing a database management system ####
Database options are many i.e. NoSQL, SQLite, MongoDB, MySQL. For this project, a relational mapping was needed in order to connect the user login information with the data of all models in a secure manner. Therefore, MySQL was chosen. SQLAlchemy is a python wrapper for MySQL that interacts with the database easily.

### Online ###

#### Baadal ####
CAST has been deployed on [Baadal](https://baadal.iitd.ac.in/baadal) cloud server of Indian Institute of Technology Delhi in an  an Ubuntu 18.04 server with 2CPU, 4GB RAM and 80GB HDD (virtual machine) of B.

### SSH ###
The secure shell protocol provides encryption to secure the connection between a client and a server. At IIT Delhi, an IP address was given that was allocated for CAST, so the given network was secured in this manner : `ssh root_name@given_ip_address`, which then adds the IP in the known hosts. 
After this, a public rsa key pair is generated for logging into the SSH account and saved. More commands like `chmod 700` and `chmod 600` are run to ensure that only the owner can read, write and execute on the directories.
Further, various configuration files are setup for the SSH in this process.

### Firewall ###
A firewall basically acts as a protective barrier between the incoming and outgoing traffic of network. For enabling a firewall a UFW (Uncomplicated Firewall) is installed in the server. As it's name suggests it is one of the most easiest way of setting up a firewall. Various rules like `ufw allow ssh`, `ufw allow 5000` are enabled so that only the SSH connections are allowed.

After more configuration file setups, the CAST project is uploaded onto this server inside a virtual environment. Upon running the project, after these steps we would still be in a development server. A development server is only useful for testing, it should not be shared with the public. 

### Web Servers ###
The final aim is to direct the HTTP requests to Flask(CAST) for which we require a web server. Nginx and Gunicorn work together for this purpose. Nginx acts as a front end web server and takes all static files like CSS, JavaScript, images etc. and then Gunicorn helps in acting as a medium by sending these requests to Flask and is basically a WSGI(Web Server Gateway Interface) HTTP Server for UNIX. There are some more final configurations done after this to ensure that the website experience is smooth and much more. 
The domain name can then be changed to anything in one of the configuration files, in this case it is : www.cast.iitd.ac.in


