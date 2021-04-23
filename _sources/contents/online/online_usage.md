## Using CAST Online (in development)

The current online version (v0.1) of CAST can be accessed from www.cast.iitd.ac.in.

### The CAST server ###

CAST is deployed on [Baadal](https://baadal.iitd.ac.in/baadal), which is a cloud orchestration and virtualization management software developed and mantained at Indian Institute of Technology Delhi ([IITD](https://home.iitd.ac.in/)). [Gunicorn](https://gunicorn.org/) and [Nginx](https://www.nginx.com/) have been used for deployment of CAST to the server. 

#### Gunicorn and Nginx ####
Gunicorn also known as Green Unicorn is a Python WSGI HTTP server for UNIX. It is highly compatible with various frameworks and is light and easy to implement.


Nginx is an open sourced web server that can be used for reverse proxying, load balancing and caching etc.

**Nginx** is the web server and it handles the request such as static files(CSS, HTML, JavaScript and images). Python code, which makes almost 90% of the CAST code, is handled by **Gunicorn**. 

