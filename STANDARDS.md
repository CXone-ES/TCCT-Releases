# About Lucidchart and the Test Case Creation Tool (TCCT)

Lucid Chart is a web-based diagramming application that the Professional Services team uses as a replacement for Visio. The Professional Services team has also developed an in-house tool called the Test Case Creation Tool (TCCT) using the Lucidchart API that extracts the contents of a call flow and rebuilds it into easy-to-use test case document. These test cases will be used for internal QA and customer end user testing (EUT).

[For information on how to use the Test Case Creation Tool, click here](./BASIC-USE.md).

## Ignoring Items or Pages

The PS Lucid Chart Template comes with a reference page for all shapes. To get the TCCT to ignore this page or anything that you may want it to ignore, do the following:

1. Select all items that you want ignored. (Ctrl + A)
2. Cut all of the selected items from the page. (Ctrl + X)
3. Select the `Layers` icon on the bottom naviation bar within Lucidchart.
4. Use the `Add new layer` button.
5. Name the new layer `Ignore`.
6. While the top of the current page in LucidChart says `Page Name > Ignore`, paste the items into the ignore layer. (Ctrl + V)

The shapes in this layer will now be ignored by the TCCT. To escape the `Ignore` layer, press escape.

## Shapes

Custom shapes were created to be able to control data that is used within the TCCT. Below you will see a basic description and image of each of the shapes used to create call flows in Lucidchart. You can create your own shapes or use Lucidchart standard shapes in your call flows, but the TCCT tool ignores those shapes. If you need a test case for the logic you are building, you must use the CXone shape library in Lucidchart. [Use the Lucidchart template referenced here in Best-Practice Techniques for Requirements Gathering for ACD-IVR Builds: Business Unit and Studio](https://niceincontact.my.salesforce.com/articles/Knowledge/Best-Practices-Techniques-for-Requirements-Gathering-for-ACD-IVR-Builds-Central-Studio).

### Annotation

Capture notes or additional details relevant to the page or a specific shape on the page.

### Assign

Stores a value in the specified variable name for later use in the flow using the format: variableName = value. 

- Multiple lines can be used to assign multiple variables using a single shape.
- String values should be surrounded by double quotes.

- The Assign shape can also use IF/ELSE, CASE, or SELECT statements to do conditional assignments. The following format should be precisely followed for use by the UAT Generator. Curly brackets must always be on their own line, not included at the end of the preceding line. 

```
IF variable = value 
{ 
  myVar = firstValue 
} 
ELSE 
{ 
  myVar = secondValue 
} 

SWITCH variable 
{ 
  CASE “123” 
  { 
    myVar = firstValue 
  } 
  CASE “456” 
  { 
    myVar = secondValue 
  } 
  DEFAULT 
  { 
    MyVar = thirdValue 
  } 
} 

SELECT 
{ 
  CASE variable = value 
  { 
    myVar = firstValue 
  } 
  CASE variable = otherValue 
  { 
    myVar = secondValue 
  } 
  DEFAULT 
  { 
    myVar = thirdValue 
  } 
}
```
### Begin

The starting point for any chart page.  Only a single Begin action should be present on a page. 

### Case

The Case shape uses the specified variable and based on the variable’s value will follow the line with the matching value.  

- You can list multiple values on a line by separating them with a forward slash ‘/’.  
- `Default` can be specified on a line to indicate the line should be used if no other line’s value matches.  
- Only a single line can be default per shape. 
- The curly brackets around the variable name are optional.  
- You cannot use expressions on the Case shape, use the If shape instead. 

### Check Hours

Performs a check of the specified hours profile. 

- Best practice is to specify the profile id and name. Example: `123 – Sales`
- Lines/branches off the shape should be labeled with the various outcomes that need to be handled. 

### Email

### Emails

### Entry

### Get Data

### Go To

### Hang Up

### If

### Loop

### Marquee

### Menu

### Note

### Play

### Prompts

### Request Agent

### Return

### RunScript

### RunSub

### ScreenPop

### Spawn

### To Page

### Transfer (Blind)

### Transfer (Managed)

### Webservice
