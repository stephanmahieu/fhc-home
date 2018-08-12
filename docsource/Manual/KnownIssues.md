# Known Issues

## Issues reported on Github
Issue can be reported and tracked on Github, see [github issue](https://github.com/stephanmahieu/formhistorycontrol-2/issues) here.

## Dialogs not showing content
There is an annoying bug in Firefox for Linux users which causes the popup window to come up
blank most of the time.

- bugzilla: [Bug 1425829](https://bugzilla.mozilla.org/show_bug.cgi?id=1425829) New popup window appears blank until right-click
- bugzilla: [Bug 1416505 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1416505) WebExtensions popup blank

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
