# IoTaWatt Custom Status

##  Purpose

This IoTaWatt webpage change allows directly opening the Status Tab, as well as provides more control over how status sections display.



##  Usage

In its simplest form, append `?s` or `?s=` to the end of the URL.
This will open the page as if the "Status" menu button was clicked. 

For advanced control, additional flags (letters) can be added after the equal sign.

A lowercase flag will expand a status section for view.  
An uppercase flag will completely hide a section and its header from view.

- `s` expands the Statistics section, and `S` hides it from view.
- `w` expands the WiFi section, and `W` hides it from view.
- `d` expands the Data Logs section, and `D` hides it from view.
- `u` expands the Uploaders section, and `U` hides it from view.

- `F` will hide the File Log info.
- `M` will hide the Main Menu buttons.

- `i` will collapse the Input/Output section.  
  (This is "reversed" behavior here, as this section is expanded by default)
- `I` will hide the Input/Output section from view.

An example to hide all sections except input/output:
`?s=FSWD`

- `x` will hide the menu and all sections except input/output.  
  (This is the same as using `?s=MFSWUD`)

NOTE:  
"Hidden from view" does NOT disable the background data updates sent to the web browser. This is not intended as a security feature!!!



##  Install

Safety first!  
Ensure you have an original `index.htm` file downloaded from the Github repo, Just In Case(tm)

https://github.com/boblemaire/IoTaWatt  - `SD/index.htm`

Connect to your IoTaWatt and in the "Tools" menu select "File Manager and Editor"

Copy/paste your editor URL into a shortcut/bookmark/text file.
If anything goes wrong and you can't access your main menu, you'll want the editor direct-link to revert your changes.
It should be `/edit.htm` at the end of the URL.

Click "Choose File" at the top left, browse to this replacement `index.htm` file and select it.
Then to the right click "Upload"

Now click Back to the main page and after the URL ending slash, add `?s` and hit enter.

If anything breaks, open the Editor direct-link and upload the original `index.htm` file from the Github repo to undo the changes.



Alternately, you can rename the replacement page to something else, `statuspage.htm` for example, before uploading it. 
Then you can access it as `/statuspage.htm?s=`


NOTE:  
This index file is v0.6.1  
At the start of the file, I appended a comment after the version number.  
At the end of the file, I have added `function checkDirectToStatus()` , and call this function at the end of `function setup()`  
