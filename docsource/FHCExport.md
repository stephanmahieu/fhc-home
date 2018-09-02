<img align="right" src="../../img/firefox-logo-32.png" alt="Firefox" title="Firefox only">
# Form History Export
This ia a standalone Java application for exporting formhistory from Mozilla's (Firefox) SQLite database.

In Firefox up to version 57 the internal persistent data store was based on SQLite, starting with Firefox version 57 that
data store is no longer accessible for add-ons (neither directly nor via the API), storage facilities for add-ons are
now based on IndexedDB.

In order to get the formhistory data from old Firefox versions and make it available for the Form History Control plugin
in newer versions, I developed a standalone application that can read from the SQLite database and create an exportfile
that can be imported by the Form History Plugin into the new data store.


## Requirements
This application can be used on any platform for which a Java runtime is available. It requires a Java runtime of at least version 1.8.
You can check if you already have a Java runtime installed by executing the following command from the commandline:

    java -version

If this command is not recognized you most likely have no Java runtime installed.
You can find instructions on how to download and install Java from [http://java.com/nl/download/](https://java.com/nl/download/)
or use a package manager provided by your OS.

## Download the export application
Download the java application fhcExport-1.0.0.jar from github here: [fhcExport-1.0.0.jar](https://github.com/stephanmahieu/fhc-home/raw/master/downloads/fhcExport-1.0.0.jar) .

Put this file in any directory you like, then open a dosbox or a terminal window and navigate to the directory where you downloaded the file.
Start the application from the commandline using the -jar option (see the Usage section).

## Usage

### Exporting data from Firefox's internal formhistory store
From the command-line you start this java application using the following command:

    java -jar fhcExport-1.0.0.jar

That should display a little help text because you have to add at least one parameter:

    -h,--help                show help.
    -o,--outputfile <arg>    optional, the path of the outputfile (default:formhistory.xml in current directory)
    -p,--profile-dir <arg>   required, the Firefox profile directory.


The application needs to know where to find the Firefox database so you have to provide the Firefox profile directory.

How to find the profile directory is described on this [mozilla.org support page](https://support.mozilla.org/en-US/kb/profiles-where-firefox-stores-user-data)

For example the profile directory can be something like: _C:\Users\John\AppData\Roaming\Mozilla\Firefox\Profiles\jguiwjin.default_ if you have a Windows OS.

If you know the profile directory you can start the java application and try to export the formhistory data.  
Execute the application with your profile directory as parameter:

    java -jar fhcExport-1.0.0.jar -p C:\Users\John\AppData\Roaming\Mozilla\Firefox\Profiles\jguiwjin.default

If everything runs smoothly you should see something like:

    Start formhistory export
    - profile directory: C:\Users\John\AppData\Roaming\Mozilla\Firefox\Profiles\jguiwjin.default/
    - destination file : formhistory.xml
    checking outputfile:        OK
    checking profile directory: OK
    reading inputfields:        2230
    reading multilinefields:    441
    writing data:               OK

You should now have an exportfile named formhistory.xml that you can use to import into the new add-on.

_The 'reading multilinefields' step might fail, this is completely normal if you never used this add-on before.
The export will still contain the formhistory for all standard text inputfields Firefox normally stores in its internal database._

### Importing the formhistory xml file:

* open the Form History Control add-on in Firefox (right-click on the Form History Control icon, choose the first menu item)
* From the dialog you just opened, choose File from the Menu on top, then choose Import: the import dialog will open
* Locate and select the formhistory.xml file you exported previously
* Selecting the xml exportfile will enable the Import button, click this button to start the actual Import