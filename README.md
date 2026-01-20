# Using the Test Case Creation Tool

The Test Case Creation Tool, or the TCCT, is an internal tool at NiCE used to generate test cases from Lucid Chart call flow diagrams. Using this tool requires a Lucid Premium account to integrate with the Lucid API. Below are instructions on how to get the TCCT up and running on your system.

## How To Download The TCCT

Releases come out as new features are added, bugs are squashed, or as needed in other cases. To find the latest release, click [here](https://github.com/CXone-ES/TCCT-Releases/releases/latest)!

Once you've found the latest release, download the file ending labelled `Test.Case.Creation.Tool-[version].Setup.exe` where version is the numeric release number, such as `1.0.0`.

Upon downloading and running this file, the TCCT is now installed locally to your system and will not need to be downloaded again. Updates are automatically pushed to the application so you don't need to do these steps for each release.

To use the Test Case Creation Tool, you must go through the authorization process within the tool. [Instructions for authorizing your Test Case Creation tool can be found in `AUTHORIZATION.md`](./blob/main/AUTHORIZATION.md).

## Basic usage

The TCCT has a variety of features to be aware of that can make your life a bit easier.

- Not sure if this is the right document? Enter the Lucid URL or Lucid document ID and press `Open Browser` to load the document directly in your browser.
- Need to get the JSON data of your chart? Enter the Lucid URL or document ID and press `Download JSON` to download the JSON to your system.
- Need to generate test cases for a chart you've run before? Open the sidebar, find the chart and press `Use` to get the document ID pasted directly into the task bar to use!
- Having some issues and not sure why? Check out the `Log Messages` section on the main menu to see details of what is going on behind the scenes.

