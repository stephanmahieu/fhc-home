# Form History Control - Release Notes

### 2.5.7.1 October 18, 2023
- Add sourcemap files: browser-polyfill, purify (issue [#149](https://github.com/stephanmahieu/formhistorycontrol-2/issues/149), [#104](https://github.com/stephanmahieu/formhistorycontrol-2/issues/104))
- Disable debug logs and fix error getting host when showing contextmenu (issue [#157](https://github.com/stephanmahieu/formhistorycontrol-2/issues/157))
- Fix errors being logged when sent messages have no receiver
- Fix column visibility list not showing active columns
- Fix error adding MutationObserver to framesets ([#153](https://github.com/stephanmahieu/formhistorycontrol-2/issues/153))
- Update Russian, Korean and Greek translations ([#113](https://github.com/stephanmahieu/formhistorycontrol-2/issues/113), [#132](https://github.com/stephanmahieu/formhistorycontrol-2/issues/132), [#135](https://github.com/stephanmahieu/formhistorycontrol-2/issues/135), [#158](https://github.com/stephanmahieu/formhistorycontrol-2/issues/158), [#159](https://github.com/stephanmahieu/formhistorycontrol-2/issues/159))

### 2.5.7.0 October 8, 2023
- Context menu reworked (use less resources, only show relevant items)
- Optionally hide address bar icon ([#133](https://github.com/stephanmahieu/formhistorycontrol-2/issues/133))
- Optionally hide right click context menu
- Update 3rd party libs: jQuery (3.7.0), DOMPurify (2.4.7), marked (2.1.3), DataTables (1.13.6)

### 2.5.6.1 April 11, 2021
- Fix storing formhistory for wysiwyg editors using iframes like the cke editor ([#103](https://github.com/stephanmahieu/formhistorycontrol-2/issues/103), [#121](https://github.com/stephanmahieu/formhistorycontrol-2/issues/121))
- Store/restore date and time related html5 fields as text inputs
- Update 3rd party libs: jQuery (3.6.0), DOMPurify (2.2.7), marked (2.0.2)

### 2.5.5.1 November 14, 2020
- Update 3rd party lib DOMPurify to 2.2.2
- Known issues:
    - translation still incomplete for: ko

### 2.5.5.0 November 14, 2020
- Downloads permission now optional, requested only when needed
- Update styling column select (vertical alignment labels)
- Fix: context-menu not always reappearing in form history dialog
- Fix: fixed bug which prevented storing the state of submitted form elements
- Update 3rd party lib markedjs 1.2.3 (markdown parser and compiler)
- Chrome only: update browser-polyfill library to v.0.6.0
- Known issues:
    - translation still incomplete for: ko

### 2.5.4.0 November 1, 2020
- Remove the unused notifications permission and notify method
- Update Greek and Russian translation
- Fix: small popup resizing with latest DataTables plugin version
- Fix: do not remember size and position for options window when opened from outside the add-on
- Fix: always allow manually adding entries
- Update 3rd party libs DataTables to latest (1.10.21)
- Known issues:
    - translation still incomplete for: ko

### 2.5.3.1 October 26, 2020
- Fix: table-view not scaling vertically (downgrade tableview plugin)
- Update Greek translation
- Known issues:
    - translations still incomplete for: ru, ko
    
### 2.5.3.0 October 25, 2020
- Larger search input, auto fit placeholder ([#94](https://github.com/stephanmahieu/formhistorycontrol-2/issues/94))
- Update button state when pasting from menu, autoselect item if exists ([#95](https://github.com/stephanmahieu/formhistorycontrol-2/issues/95))
- Export now uses the downloads API (downloads permission added)
- Replace select-column button by icon, add check mark to each column button
- When text is selected (and highlighted) Ctrl-C will copy the selected text ([#98](https://github.com/stephanmahieu/formhistorycontrol-2/issues/98))
- Extra option to remember window size and position
- Extra option for field fill mode
- Update 3rd party libs: DOMPurify, jQuery, DataTables
- Known issues:
    - translations still incomplete for: ru, ko, el
    - entries list not scaling vertically

### 2.5.1.1 October 25, 2020
- Security patch: Update DOMPurify 3rd party library to 2.2.0

### 2.5.1.0 January 12, 2020
- Additional dateformatting options ([#96](https://github.com/stephanmahieu/formhistorycontrol-2/issues/96))
- Small update Russian translation.json ([#91](https://github.com/stephanmahieu/formhistorycontrol-2/issues/91))
- Hide Select text highlighting older browsers (Ctrl+a) ([#74](https://github.com/stephanmahieu/formhistorycontrol-2/issues/74))
- Fix: show correct application icon when activetab is refreshed (domainfilter active)
- Fix: disable leftover debug console log statement

### 2.5.0.0 January 10, 2020
- Formhistory popup improvements:
    - Show/hide individual columns in the formhistory popup ([#78](https://github.com/stephanmahieu/formhistorycontrol-2/issues/78)) 
    - Additional length column displaying the no. of characters ([#77](https://github.com/stephanmahieu/formhistorycontrol-2/issues/77))
    - Reduced scrollbar inertia ([#79](https://github.com/stephanmahieu/formhistorycontrol-2/issues/79))
    - Context menu:
        - act upon selection if present otherwise upon right-clicked item ([#73](https://github.com/stephanmahieu/formhistorycontrol-2/issues/73)) 
        - hide context menu when mouse leaves the menu ([#75](https://github.com/stephanmahieu/formhistorycontrol-2/issues/75)) 
    - Additional standard shortcut keys support:
        - Ctrl+A selects all items ([#74](https://github.com/stephanmahieu/formhistorycontrol-2/issues/74))
        - Ctrl+C copy formhistory of first selected item to clipboard 
        - Shift+Ctrl+C copy formhistory of first selected item to clipboard without formatting
        - Del key deletes selected item(s)
    - Fixed: Alt-key shortcuts for main dropdown menu not working
- Improved highlighting filled-in items ([#70](https://github.com/stephanmahieu/formhistorycontrol-2/issues/70))
    - Highlighting changes back to normal after 5 seconds 
    - Improved readability (change background, text color and border-color) 
- Form History Control context menu item can be turned off conditionally ([#68](https://github.com/stephanmahieu/formhistorycontrol-2/issues/68)) 
- [Domain filter support](https://stephanmahieu.github.io/fhc-home/Manual/manual/#domain-filter) for `*`-wildcard (match subdomains) ([#71](https://github.com/stephanmahieu/formhistorycontrol-2/issues/71)) 
- [Field filter support]((https://stephanmahieu.github.io/fhc-home/Manual/manual/#field-filter)) for `*`-wildcard, host and _&lt;empty&gt;_ keyword ([#62](https://github.com/stephanmahieu/formhistorycontrol-2/issues/62))
- Chrome browser now also supports disabling the shortcut keys ([#56](https://github.com/stephanmahieu/formhistorycontrol-2/issues/56))
- Fixed: writing to clipboard, additional clipboardWrite permission added to manifest
- Fixed: application icon not showing correct state (active domain filter):
    - with multiple opened windows
    - when page in a tab window was updated
- Fixed: unnecessary scrollbars in pageaction popup   

### 2.4.2.0 December 29, 2019
- Update Russian translation 

### 2.4.1.0 December 29, 2019
- Update Russian translation 

### 2.4.0.0 December 28, 2019
- Additional ISO date format _(yyyy-MM-dd HH:mm:ss)_
- Additional menu item to copy entry without formatting
- Advanced preferences only made available in advanced mode _(checkbox)_
- Re-ordered option categories
- Additional preferences:
    - choose fieldtype to retain _(multiline and or single)_ ([#53](https://github.com/stephanmahieu/formhistorycontrol-2/issues/53))
    - configure update-interval ([#39](https://github.com/stephanmahieu/formhistorycontrol-2/issues/39))
    - configure mousewheel scroll amount
    - save formhistory in incognito mode _(default off)_
    - ability to disable most shortcut keys ([#56](https://github.com/stephanmahieu/formhistorycontrol-2/issues/56))
- New translations: Russian ([#61](https://github.com/stephanmahieu/formhistorycontrol-2/issues/61)), Korean
- New Orange theme
- Bugfix: custom ACE-handler for collecting data from [ACE](https://ace.c9.io/) powered sites
- Bugfix: icon notification (enabled/disabled) when multiple active windows 
- Bugfix: context menu creation (issues [#36](https://github.com/stephanmahieu/formhistorycontrol-2/issues/36), [#40](https://github.com/stephanmahieu/formhistorycontrol-2/issues/40), [#57](https://github.com/stephanmahieu/formhistorycontrol-2/issues/57))

### 2.3.1.0 May 28, 2019
- Update third party libraries
- Fulfill requirements Mozilla Third Party Library Usage
    - Previous versions (2.0.3.2, 2.1.0.0, 2.1.0.1, 2.2.0.0, 2.3.0.0, 2.3.0.1) did not meet these requirements and are disabled on mozilla.org

### 2.3.0.1 May 19, 2019
- Bugfix: 'Select All' does not respect search filter

### 2.3.0.0 September 21, 2018
- Shortcut keys added for a variety of actions, configurable via preferences
- Cleanup added to the drop down menu of the main dialog
- Some minor layout improvements

### 2.2.0.3 September 2, 2018
- Chrome compatible, now FHC is also available in the Chrome Web store
- Replaced the svg icons in the chrome manifest with png icons

### 2.2.0.0 August 31, 2018
- Bugfix field detection: child input elements were missing from dynamically added forms  
- Added configurable Multiline thresholds settings to the Preferences 
- Translation added for the age column in the main dialog
- Layout improvements main dialog:
    - Use stylish custom scrollbars in main dialog (replaces ugly system scrollbars)
    - Removed label from search box, added placeholder
    - Hide page control in the main dialog when page-size is set to show all
    - Open Help/Release-notes pages in the same window (different tabs)
    - Refresh display after a manual cleanup
- Improved Chrome compatibility

### 2.1.0.1 August 25, 2018
- Previous version was not marked as compatible for All platform. This version is equal to the previous version but has
been uploaded to Mozilla now provided with the correct platform-compatibility info

### 2.1.0.0 August 19, 2018
- Improved field detection
- Automatic Cleanup added
- Disable collecting formhistory for specific sites or fields
    - preferences window:
        - Domain filter: all / blacklist / whitelist
        - Field filter: exclude fieldnames
    - toolbar icon now reflects status enabled/disabled
- Redesign preferences window
- Limit the amount of data for the popdown dialog (browser limitation issue)
- Show fields current page: color code specific input types
- Update last-used date for autofilled fields
- Blue theme added

### 2.0.3.2 December 22, 2017
- Bugfix: remove prematurely (incomplete) option features

### 2.0.3.1 December 22, 2017
- Update German translation (datatables.json)

### 2.0.3.0 December 20, 2017
- Added German translation

### 2.0.2.5 December 16, 2017
- Bugfix 2 for not showing content in popup windows on some OS's and slow pc's (multiple attempts to restore content)
- Bugfix missing first letter of About window title

### 2.0.2.4 December 15, 2017
- Bugfix for not showing content in popup windows on some OS's

### 2.0.2.3 December 7, 2017
- Display an error message when there is a problem with database permission
- Hide URL column in small popup tableview to prevent messed up layout (remains searchable)

### 2.0.2.2 November 21, 2017
- Tweak column widths in small datatable popup to prevent messed up layout
- Hold page position when updating and redrawing age in datatable
- Rename Wiky.js -> wiky.js (fix wiki preview in entryview)
- Small increase (50px) entryview width

### 2.0.2.1 November 21, 2017
- Bugfix: limit size of columns and preview in the small popup panel)

### 2.0.2.0 November 21, 2017
- Add url to the tableview, searching now includes the url
- Added Markdown, Wiki and Text preview to entryview
- Remove inline styles when converting html to readable text
- Escape tooltip text in datatable view (fix values sometimes exceeding max length value column)

### 2.0.1.0 November 20, 2017
- Add additional clickable icons to the small popup
- Copy text to clipboard now preserves HTML formatting
- Hide HTML tags from tableview, show readable text only
- Bugfix restore editor field contextmenu:
    - show international chars
    - sort hostname matches by date
    - exclude hostname matches from recent used
- Fix close button preference dialog not always visible

### 2.0.0.3 November 15, 2017
- Show all data in the left-click popup dialog instead of just the fields for the active page (more intuitive)
- Set the override-automplete preference default to false

### 2.0.0.2 November 14, 2017
- Fixed issue where text entered in dynamically generated input forms (like gmail) was not detected

### 2.0.0.1 November 13, 2017
- Bump version to 4 digits to comply with old (non-WebExtension) version

### 2.0.0 November 12, 2017
- Complete redesign, WebExtension and Multiprocess compatible