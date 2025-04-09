# Frequently Asked Questions (FAQ)

## Single line entries lack a URL?
This behavior is by design. 

Single line fields are very often re-occuring (same name and/or id) on other websites.
Think of e-mail or address fields.
These fields are very likely to be used on other websites in similar contexts.
For suggesting formhistory entries when typing in a single line field or form filling the originating domain or url is
of little or no use. This is also the way Firefox built-in formhistory stores its data.

Another reason is that the local storage system is not very well suited for relational data (1 to many) which would
be required to store multiple url's for a single line field when used by multiple websites.

_Older version of this add-on (pre webextension) deduced the domain of a single line fields where it was last used by
comparing the last used date with the browse-history._

## Why is input not captured after a fresh install?
After installing the Form History Control extension for the first time, no input is registered when typing input.

The reason is that a content script provided by the extension has to be loaded for the webpage in order to
capture data typed in editor fields. These scripts however are not automatically loaded when an extension is installed
for the first time.

So after installing this extension for the very first time, refresh the page or restart the browser. Restarting the
browser enables form history capturing for all webpages loaded in tabs.  

## Data not stored for website xyz?
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

## Old Lazarus extension compared with FHC

Many people argue that the old Lazarus extension which also captured form history did a better job.

Lazarus stems from a different era, from the time when internet pages were mostly static and not dynamically generated
and relying heavily on scripting as they are today.  

In today's world, Lazarus would not be able to capture the vast majority of multi-line inputs.
Development of Lazarus was abandoned because their maintainers were no longer willing to put in the time and effort
it takes to keep up with modern day web developments.
If memory serves me right, they even tried to make a paid version but it dien not attract enough backers to make it
worth their while.
