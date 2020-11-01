# Frequently Asked Questions (FAQ)


## Data not stored?
Some websites use advanced techniques and frameworks involving javascript that make it virtually impossible to capture
user input in a generic way.

On request I might be able to add workarounds for popular websites/frameworks, please submit an issue and let me know for
which website(s) capturing entries does not work.

## Empty database?
This add-on now uses the new mandatory WebExtensions API which no longer offers access to
browser's built-in formhistory database. This means that after installing this new, you start with an empty
formhistory data storage.

There are two ways to get the formhistory data from the old **Firefox** version back into the new version:

1. If you have an export file from the old version, you can simply import that file into the new
   version. The exportfile is compatible with the new version.
1. If you have no export file you may use the standalone __*FHCExport*__ Java application that
   is capable of exporting the formhistory data and make it available for the new version,
   go to the [FHCExport page](../FHCExport.md) for more information.

