# Assignment 2 Scripts

### Prerequisites
* Bash
* A clone of the directory files saved in the user's home directory
* Sudo access


### Project 1: configuration_script_main
This script is for the setup of a new system by automatically installing selected packages and organizing configuration files. It installs the packages specified by the user in the *packages* text file and creates symbolic links to the cloned directory. **This script requires you to run it as the root user or using sudo.**
<br>

**How to Call The Script to Download Packages** <br>
- Use the "-p" option and provide the name of the package text file that contains a list of packages for download.
* *e.g. "sudo ./configuration_script_main -p package"*
<br>

**How to Call The Script to Set Configuration Symbolic Links** <br>
* Use the "-c" option and provide the name for a single user to create the symbolic links for.
* *e.g. "sudo ./configuration_script_main -c user"*
<br>

**How to Set Custom Packages to Download:**
* Edit the text in the *packages* file to specify which packages you want downloded onto the system automatically. Separate each package on it's own new line.
<br>

###### NOTE: There are already default packages listed in the file for download
<br>

---

### Project 2: configuration_script_new_user
This script creates a new user on a computer and allows you to customize the username, shell, add the new user to existing groups, sets a password, and automatically sets up a home directory. It copies default configuration files from `/etc/skel` into the new home directory and assigns the new user to a primary group that matches their username. **This script requires you to run it as the root user or using sudo.**

###### NOTE: A user name must always be provided with the "-u" option to run this script
<br>

**How to Set the New User's Name** <br>
* Use the "-u" option when calling the script and provide the name.
* *e.g. "sudo ./configuration_script_new_user -u username"*
<br>

**How to Choose a Customer Shell for the User** <br>
* Use the "-s" option and provide the chosen shell.
* *e.g. "sudo ./configuration_script_new_user -u username -s bash"*
<br>

**How to Add the New User to Existing Groups During Creation** <br>
* Use the "-g" option and provide the chosen shell.
* *e.g. "sudo ./configuration_script_new_user -u username -g "group1 group2 group3" "*
<br>

---

### Configuration
* package - customize this file to specify which packages should be installed

### Troubleshooting
* exit 1 - Indicates an error because of how the script was called. Either it was not called with sudo or no options were given to the script
* exit 2 - Indicates an error because the option given to the script did not receive a required argument or an invalid option was given.
* exit 3 - Indicates an error because a user who already exists was provided or a group that doesn't exist was provided to the configuration_script_new_user script.