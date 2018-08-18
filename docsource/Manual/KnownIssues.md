# Known Issues

## Issues reported on Github
Issue can be reported and tracked on Github, see FHC [github issues](https://github.com/stephanmahieu/formhistorycontrol-2/issues).

## Dialogs not showing content
There is an annoying bug in Firefox for Linux users which causes the popup window to come up
blank most of the time.

- bugzilla: [issue 1425829](https://bugzilla.mozilla.org/show_bug.cgi?id=1425829) New popup window appears blank until right-click
- bugzilla: [issue 1416505](https://bugzilla.mozilla.org/show_bug.cgi?id=1416505) WebExtensions popup blank

Workaround is to right-click inside the window or resize it. Hopefully this bug will be fixed soon.

## Progress spinner never stops spinning

While opening the popdown dialog (left-click), the progress spinner sometimes never stop spinning.

The amount of resources available for a popdown (left-click) dialog is limited by the browser.
When there is too much data to display, the applications runs silently out of resources.
The total amount of data that can be displayed by the popdown dialog without a problem lies around 2500 items 
depending on the available resources of the underlying system.

To fix the problem open the main dialog instead (right-click, choose first menu item). The main dialog is not affected by the 
resource limitation and will always show all available formhistory data.
You can now delete some of your older entries to reduce the amount of data.

This issue is fixed in release 2.1.0.0 which will automatically limit the amount of data displayed by the popdown dialog
and show a warning message when data was discarded from the view. The new version will also provide the ability to
automatically cleanup history.

## Storage (IndexedDB) Error

IndexedDB error occurs for the following reasons.

- Cookies are disabled
- Firefox setting is set not to remember history
- IndexedDB is not enabled in about:config
- Corrupted file exists in firefox's storage

If any of these apply, IndexedDB can not be used.

### Cookies not enabled

A [firefox bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1406675) prevents an add-on to access the
internal storage when cookies are disabled. Until this bug is fixed it is necessary to enable cookies in order for
this add-on to be granted access to internal storage.

To enable cookies open Privacy & Security of Firefox settings, it is necessary to enable:
**_Accept cookies and site data from websites (recommended)_** 

### Firefox setting is set not to remember the history

Please confirm that firefox setting is set to remember history.

Open Privacy & Security of firefox settings, it is necessary to set History as follows:    
_Firefox will:_ **_Remember history_**  
&nbsp;&nbsp;**or**  
_Firefox will:_  **_Use custom settings for history_**  
&nbsp;&nbsp;&nbsp;&nbsp;[X] **_Remember my browsing and download history_**  
&nbsp;&nbsp;&nbsp;&nbsp;[X] **_Remember search and form history_**  

### IndexedDB is not enabled in about:config

Please access about:config and confirm that the value of `dom.indexedDB.enabled` is true.
If false, change it to true and restart firefox.

### Corrupted file exists in firefox's storage

The cause of corruption generally fall under one of the following reasons (see [bugzilla 944918](https://bugzilla.mozilla.org/show_bug.cgi?id=944918)):

1. running some cleaning or optimizing software, for example CCleaner, BleachBit, Wise Disc Cleaner, ZHP Cleaner, Wisecleaner. Regarding popular CCleaner, reported versions were quite old: 5.03.5128 and 5.28.
1. running some special (less known) anti-virus or anti-malware software, like Malwarebytes or SUPERAntiSpyware. However only very few people reported this and was not able to reproduce it (but it may be related to data stored in the db, like some URL that is flagged as malware...).
1. downgrading your Firefox profile - if you execute any Firefox older than 57, then your profile gets instantly corrupted! This is often the reason - users using 56 or ESR versions decides to upgrade to 57+, they see half of their add-ons doesn't exists anymore, so they downgrade back and BAM! Database corrupted.
1. there are some rare cases when profile gets corrupted during the Firefox upgrade.
1. few people reported that only database of my add-on was corrupted and other add-ons / pages using IndexedDB were still working (I'm testing this on this page (db log is in bottom left corner): http://mdn.github.io/to-do-notifications/)

Regarding fixing it, if only one database is corrupted, then you may need to just remove specific database (dropping DB using API will fail, so you need to do it manually on your hard drive in profile\storage\default\<folder with db>).
If your whole IndexedDB engine is corrupted, the only option may be resetting your profile (consider setup Firefox Sync. before).

For information on fixing a corrupted profile see [this article](https://github.com/sienori/Tab-Session-Manager/wiki/IndexedDB-Error#corrupted-file-exists-in-firefoxs-storage)
by sienori, developer of the Tab-Session-Manager add-on.

## Reporting new issues

Please consult the Know Issues and [FAQ](./FAQ/) presented here carefully before creating a new issue,
your problem may very well be identified earlier. 

New issues can be reported on Github (account required), see [github issues](https://github.com/stephanmahieu/formhistorycontrol-2/issues).
You may also report issues by adding a comment to the release on the [Form History Control blog](https://formhistory.blogspot.com/search/label/Release)
or just drop me an e-mail (formhistory@yahoo.com).

When reporting issues please let me know what OS you use. the browser version and the version of the
Form History Control add-on.

Please do not use the rating system on the Firefox add-ons page to report problems. Reviews that contain Bug reports
or Support requests are considered inappropriate and will be flagged and removed by Mozilla.