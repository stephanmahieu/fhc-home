# Release Notes

## 2.0.3.2 December 22, 2017
- Bugfix: remove prematurely (incomplete) option features

## 2.0.3.1 December 22, 2017
- Update German translation (datatables.json)

## 2.0.3.0 December 20, 2017
- Added German translation

## 2.0.2.5 December 16, 2017
- Bugfix 2 for not showing content in popup windows on some OS's and slow pc's (multiple attempts to restore content)
- Bugfix missing first letter of About window title

## 2.0.2.4 December 15, 2017
- Bugfix for not showing content in popup windows on some OS's

## 2.0.2.3 December 7, 2017
- Display an error message when there is a problem with database permission
- Hide URL column in small popup tableview to prevent messed up layout (remains searchable)

## 2.0.2.2 November 21, 2017
- Tweak column widths in small datatable popup to prevent messed up layout
- Hold page position when updating and redrawing age in datatable
- Rename Wiky.js -> wiky.js (fix wiki preview in entryview)
- Small increase (50px) entryview width

## 2.0.2.1 November 21, 2017
- Bugfix: limit size of columns and preview in the small popup panel)

## 2.0.2.0 November 21, 2017
- Add url to the tableview, searching now includes the url
- Added Markdown, Wiki and Text preview to entryview
- Remove inline styles when converting html to readable text
- Escape tooltip text in datatable view (fix values sometimes exceeding max length value column)

## 2.0.1.0 November 20, 2017
- Add additional clickable icons to the small popup
- Copy text to clipboard now preserves HTML formatting
- Hide HTML tags from tableview, show readable text only
- Bugfix restore editor field contextmenu:
    - show international chars
    - sort hostname matches by date
    - exclude hostname matches from recent used
- Fix close button preference dialog not always visible

## 2.0.0.3 November 15, 2017
- Show all data in the left-click popup dialog instead of just the fields for the active page (more intuitive)
- Set the override-automplete preference default to false

## 2.0.0.2 November 14, 2017
- Fixed issue where text entered in dynamically generated input forms (like gmail) was not detected

## 2.0.0.1 November 13, 2017
- Bump version to 4 digits to comply with old (non-WebExtension) version

## 2.0.0 November 12, 2017
- Complete redesign, WebExtension and Multiprocess compatible