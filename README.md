**** Github repository AC_UsersGuide content:

README this file with installation and usage instructions.
OATS-CADC-Guides_brand 	directory containing the OATS-CADC Guides brand
publican.cfg 		this guide specific configuration
en-US  			english version

**** Usage instructions in CentOS7:

** Install publican. 

$ yum install publican publican-doc publican-brand
Replace brand with a known brand, for example, redhat, fedora, jboss, ovirt, or gimp.


** Clone the repository.
git clone https://github.com/oats-cadc/cadc-log-admin-guide

** Install the brand. 
The brand files must be placed in a subdirectory of the Publican Common Content
directory (in CentOS7 the AC custom brand directory must be placed in
/usr/share/publican/Common_Content). 

sudo cp -r ${MY_REPO}/OATS-CADC-Guides_brand /usr/share/publican/Common_Content

** Compile the book.

* In a single html page:
publican build --formats html-single --langs en-US --config publican.cfg

* In html:
publican build --formats html --langs en-US --config publican.cfg

* In pdf:
publican build --formats pdf --langs en-US --config publican.cfg

* In a single .txt file:
publican build --formats txt --langs en-US --config publican.cfg

* In more formats:
publican build --formats txt,html,html-single,pdf --langs en-US --config publican.cfg

The compilation output will be located in ${MY_REPO}/tmp/<lang_code>/<format>

# oats-cred-users-guide
