# CHANGELOG

| Version | Summary |
|   ---   |   ---   |
| [`1.1.0`](#v110) | Base Release |
| [`1.2.0`](#v120) | UI Overhaul + Sidebar |
| [`1.2.3`](#v123) | Variable tracking & Assignment printing |
| [`1.3.0`](#v130) | Feedback Reporting + Help |
| [`1.3.1`](#v131) | Invalid Shape Patch + Only Dark Mode |
| [`1.4.0`](#v140) | New Export Option + Ignore Fix |
| [`2.0.0`](#v200) | Expanded Action Support + Smarter Generation |

# v1.1.0

The base release of the Test Case Creation Tool. This release has all of the essential items that is needed for usage. Auto-updating, Excel output, and Lucid integration are all in this version of the tool.

## Added ✅

- Integration with Lucid API.
- Export to `.xlsx` files using ExcelJS.
- Automatic updating using Electron library.
- Logging + log window on Main Menu.
- Settings & configuration window.

# v1.2.0

This release has a large user-interface overhaul for the tool. User feedback reported a lack of user-friendly interfaces, so this update was created in response.

## Added ✅

- Sidebar for previously used charts.
- Variable substitution in charts has been added.
- Wrike output has been added.

## Changed ✏️

- Main Menu user interface updated to be more modular.
- Settings menu user interface updated to be more modular.
- `ASSIGN` action issues resolved.

# v1.2.3

This release is in preparation for rollout to as many users as possible. Quality of life items have been added.

## Added ✅

- Validation window for warning and errors was created.
- Logging updated so that crash logging and other logging can be put into local file.
- Variable assignments can now be printed to `.xlsx` with generation settings.
- Default settings added.

## Changed ✏️

- Quiet crashing issue resolved.
- UI issue with the sidebar icons resolved.
- UI updated to be inline with NiCE and ES Tool.
- Each test case path now contains an independent variable tracker.

# v1.3.0

Several small adjustments were made including changing the "Configuration" menu to "Settings", updating the Warning modal, and adjusting some logging logic.

## Added ✅

- Documentation for authorizing the Test Case Creation Tool was uploaded.
- A new menu option was created: The `Help` tab.
  - A feedback reporting system was created and can be accessed under the `Help` tab. It is labelled `Report Feedback`.
  - A direct link to the most recent changes has been added under the `Help` tab. It is labelled `Recent Changes`.

## Changed ✏️

- Log verbiage was updated to be more concise.
- The drop down menus within the `Settings` page are now animated.

## Removed ❌

- Log timestamps no longer show down to the millisecond.
- The internal logger no longer times startup times since they are inconsistent between cold starts and repeated use.

# v1.3.1

This patch resolves an issue that floods the log with invalid shape errors instead of using the Warning and Error modal.

## Changed ✏️

- Invalid shape warnings moved from log into warning modal.
- Styling stays in dark mode.

# v1.4.0

Added export issues button
Fixed ignore issues. Now all items should be acknowledged.

## Added ✅

- Warnings and errors from the pop-up window can now be exported to an `.XLSX` file.

## Changed ✏️

- Some underlying processes had discrepancies regarding items labelled on the 'ignore' layer. Changes to this now make it so that those items are properly ignored more consistently.

# v2.0.0

A major update focused on significantly expanding chart support and improving output quality. Many previously unrecognized action types are now fully handled, and test case generation is smarter and more accurate across the board.

## Added ✅

- Many additional action types are now fully supported, including Menu, Hours, Email, If/Loop,
  RunScript, Music, Blind Transfer, Message, Play, Return, and several others. These previously
  appeared as unidentified actions in output.
- Test case strings are now generated for Menu and Hours actions.
- Wrike output is now complete.
- A secondary validation pass has been added. More issues will now be surfaced in the warning
  and error modal that were previously missed.

## Changed ✏️

- Path generation is now smarter. The tool no longer generates redundant paths for both branches
  of a condition when sufficient data exists to determine the correct one. Users will see fewer
  duplicate test cases in their output.
