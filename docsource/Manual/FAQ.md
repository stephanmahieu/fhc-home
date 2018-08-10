# Frequently Asked Questions (FAQ)


## Data not stored?
If you experience problems regarding form history not being saved, please check if you have
cookies enabled. This add-on uses indexeddb to store its information and according to this
issue (see bugzilla) disabling cookies will prevent data being stored. So please check the
Privacy and Security preferences of the browser and make sure that cookies are accepted or
Form History Control will not be able to store your data.

## Empty database?
This add-on now uses the new mandatory WebExtensions API which no longer offers access to
Firefox's built-in formhistory database. This means that after installing the WebExtensions
enabled version, you start with an empty formhistory data storage.
There are two ways to get the formhistory data from the old version back into the new version:

1. If you have an export file from the old version, you can simply import that file into the new
   version. The exportfile is compatible with the new version.
1. If you have no export file you may use the standalone __*FHCExport*__ Java application that
   is capable of exporting the formhistory data and make it available for the new version,
   go to the [FHCExport page](../FHCExport.md) for more information.

