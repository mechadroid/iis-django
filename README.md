# iis-django
installing and running django on windows server 2016


# First install IIS server with CGI Features

# then install Python

# then install Django

# then install wfastcgi via PIP

# then check the directory permission

# the steps sequence above are the results of few hours of troubleshooting why i cant run a basic django setup on my Windows Server 2016

# THIS IS FOR PERSONAL REFERENCE BASED ON THE MISTAKES I MAKE AND HOW DID I SOLVE IT
# Firstly, I install a Windows Server 2016, then I enabled the IIS, (this is my first time installing IIS, hoping it was as straightforwrd installation as NGINX and APACHE, i was wrong)
# Configure my default website
# Serve my inital welcome screen on the browser
# Install python 
# Install django
# Create my initail project
# server the page using runserver
# django serves the welcome screen
# all is well at this point
# everything is A ok on individual stages
# let them work as one
# Problem! Problem! Problem!
# Create a file named "web.config", (this is the config file, like .httpd file in apache)
# this file holds the configuration on how your configured site/folder works
# here you put the fastcgi details to point to your django installation
# but i still never works, at this stage, no error reference whatsoever
# after some patience wasted it turns out that on IIS the CGI feature was not installed
# after installing the CGI feature and restarting the server 
# i have my first basic django text welcome screen on IIS 
# but there is no static files being serve
# another percentage of patience was utilized, (read, test, read, test... whatever)
# turn to the directory permission to allow modification
# boom it works well
# thank you self.

