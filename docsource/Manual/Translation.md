# Help translating 
If you want to participate in translating Form History Control you can find some detailed instructions here.

## Download the add-on
First download the source code of the add-on to a location of your choosing. You can download the latest version from
[github.com](https://github.com/stephanmahieu/formhistorycontrol-2) and use the green "Clone or Download" button.

Either use a git client (if you have that installed and know how to use it) or just simply download the zipfile
and unpack it.

## Install and change language (Firefox) <img style="vertical-align:top" src="../../img/firefox-logo-32.png" alt="Firefox" title="Firefox">
If you want to test your translation, you can do so in a separate Firefox profile. See
[support.mozilla.org](https://support.mozilla.org/en-US/kb/profile-manager-create-and-remove-firefox-profiles) on how to
create an extra profile. Within this profile you can load the add-on version you downloaded in the first step.
 
Install the downloaded add-on by entering "_about:debugging_" in the URL bar and then click "_Load Temporary Add-on_".
Choose the "manifest.json" file of the add-on you downloaded in the first step
(see also this [mozilla webpage](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Temporary_Installation_in_Firefox) for detailed instructions).
The add-on is now installed and available in your profile.  
If you exit Firefox the add-on will not be available if you
start Firefox again, you have to load the temporary add-on again. The data will remain available if you exit Firefox,
only when the add-on is removed using the "about:debugging" page, data will be removed as well.    

If you are using an international version of Firefox, it may very well be that you are not seeing the desired translation 
but the (default) english translation instead. In that case you can switch the default language by entering "about:config" 
in the URL bar, search for `"general.useragent.locale"`, and set the value to the tag for the desired language,
for example "de" for German. You may also have to change the `intl.locale.requested` property accordingly.

In some cases switching the locale does not work for whatever reason but it probably has something to do with not
being able to display international characters. If switching the language does not work you are probably using an
international version, in that case download and install a Language specific version of Firefox.

If you made changes in one of the language specific files you may have to reload the add-on (on the about:debugging page)
in order to see the changes.

## Install and change language(Chrome) <img style="vertical-align:top" src="../../img/chrome-logo-32.png" alt="Chrome" title="Chrome">    
If you want to test your translation, you can do so in a separate user profile. See
[Google Chrome Help](https://support.google.com/chrome) on how to create an extra profile (people).

To load the Form History Control extension use the _More tools_ option from the settings menu by clicking the tiny dots
(or bars, in some cases) in the top right next to the URL bar. From the More tools submenu choose _Extensions_ to open
the extensions page. On top of the extensions page, use the _Load unpacked_ button to select the directory where you
downloaded the add-on.

To switch the language in Google Chrome:

* Open the Settings page by clicking the tiny dots (or bars, in some cases) in the top right next to the URL bar
* Scroll down to the very bottom and open _Advanced_ settings
* More options are shown, go to the _Languages_ section
* Use the menu next to the desired language (tiny dots) and select _Display Google Chrome in this language_ (if you do
not see the desired language, use the _Add languages_ link to add it to the list)

If you made changes in one of the language specific files you may have to reload the add-on (on the extensions page) in
order to see the changes. Click the refresh icon to reload the extension.

## The language specific files
The file you should translate is located in the \_locales\xx\ subdirectory where xx is the language tag of the country,
the file should be named **messages.json**. If the xx directory not exists yet, create it and copy the files 
from `\_locales\en\ ` into the new xx directory. Find more on this subject including a list of country tags
here: [Reference Global Objects Intl](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl).

The messages.json file contains multiple labels each having a message and a description part. Only translate
the message part! The description is only meant to give the translator an indication of what and where the message is
used for. Please do not add empty lines or break up existing lines into multiple lines.

The `\locales\xx\ ` subdirectory also contains a **datatables.json** language file, this file is used by the jquery
datatables plugin. For this plugin there are already many translations available.
For a complete list see: [https://datatables.net/plug-ins/i18n/](https://datatables.net/plug-ins/i18n/).

## Submit your translation
When finished translating submit the translated files so I can incorporate the new or updated language files in the
next release.

If you are using git do a pull request, otherwise send the translated _messages.json_ and _datatables.json_ files directly
to my email address.
