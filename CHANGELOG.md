# CHANGELOG

| Version | Summary |
|   ---   |   ---   |
| [`1.1.0`](#v110) | Base Release |
| [`1.2.0`](#v120) | UI Overhaul + Sidebar |
| [`1.2.3`](#v123) | Variable tracking & Assignment printing |

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
