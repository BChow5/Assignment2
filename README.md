# Assignment 2 Instructions

## Scripts You Can Run:

### configuration_script_main
This script is for the setup of a new system by automatically installing selected packages and organizing configuration files. It installs the packages specified by the user in the *packages* text file and creates symbolic links to the cloned directory. This script requires you to run it as the root user or using sudo.

**How to Call The Script to Download Packages**
*e.g. "sudo ./configuration_script_main -p package"*

**How to Call The Script to Set Configuration Symbolic Links**
*e.g. "sudo ./configuration_script_main -c"*

**How to Set Custom Packages to Download:**
Edit the text in the *packages* file to specify which packages you want downloded onto the system automatically. Separate each package on it's own new line.
<br>
###### NOTE: There are already default packages listed in the file for download
<br>

### configuration_script_new_user
This script creates a new user on a computer and allows you to customize the username, shell, add the new user to groups and automatically sets up a home directory. It copies default configuration files from `/etc/skel` into the new home directory and assigns the new user to a primary group that matches their username. This script requires you to run it as the root user or using sudo. 
<br>

#### Customization Files
* package - allows user to customize which packages should be installed