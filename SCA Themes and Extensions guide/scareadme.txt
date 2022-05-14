//Install the bundles

03: Install SuiteCommerce Bundles
Scenario: The SuiteCommerce bundle brings the bulk of the commerce functionalities into a
NetSuite account, but it still needs other bundles in order for Extensions and Themes to work.
Below are the key bundles that needs to be installed


1 In the NetSuite interface, navigate to Customization > SuiteBundler > Search & Install
Bundles.

2 On the Search & Install Bundles page, search for the SuiteCommerce bundle and enter
311589. This is the bundle’s id.

3 Click Install on the Bundle Details page.
4 Click OK.

Make sure to read the terms and conditions if displayed, and click I Agree.

5 Click Install Bundle on the Preview Bundle Install page.

6 Monitor the progress of the installation. Perform the same process for the remaining
bundles below, installing them in the following order:

 SuiteCommerce Configuration (311614)
 SuiteCommerce Extension Management (317001)
 SuiteCommerce Base Theme (317888)



08: Initial Activation
Scenario: The initial activation kickstarts everything from the backend perspective of the site.
Successful activation means the site is now accessible through the URL specified on previous
steps.
1 Navigate to Setup > SuiteCommerce Advanced > Extension Manager.
2 Click New Activation.
3 Select the site record from the SELECT A WEB SITE field.
4 Select a Domain.
5 Click Next.
6 Click the Themes subtab.
7 Click the ACTIVE checkbox for SuiteCommerce Base Theme.
8 Click Activate.
9 Monitor the activation process until its done.

//Notes about Dev Tools:

1) Gulp runs on top of NodeJS
2) NPM(Node Package Manager) comes with the Installation of NodeJS
3) NPM is a command line tool which Install and uninstall packages (Dependency packages)

Commands:
------------
Install the nodeJs 
npm -v (Display the version of npm library Installed)
npm install (Install the necessary dev tool components)    - Pull all the dependencies in the node_modules folder
npm install lodash (Will install thirdparty library lodash)


Gulp JS:
--------------
1) (Manages local server and concatenating all files and runs on top of NodeJS. Compiled all the files in single file.)

2) Watches the changes in the file and add the changes in the single file.

Gulp Commands:
-----------------
gulp -v (returns gulp version)
gulp theme:fetch (Fetches the active theme)
gulp extension:fetch (fetches all the active extensions)
gulp theme:fetch --to (fetch the active theme using a different user credential)









IMP New Things:


SuiteCommerce MyAccount only supports the SC Base Theme and certain SC Extensions. You can activate the SC Base Theme for a domain. You can also activate custom and third-party themes that are compatible with SCMA.





{"SCA":">=20.2.1","SCS":">=20.2.1"}

20.2.1