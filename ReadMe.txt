This gadget is being developed to fill a gap in Google Sites where there is a complete lack of a commenting system.
References: the code base was branched from "Awesome Table (with interactive controls, using Google Sheets)"

The cell range is the entire range of data that is required to be passed into the control for processing.
e.g. A1:H

If you do not want a given column actually output onto the page but the control still needs it, then prefix the name with 'Hidden'.

use 'inherit' as the background color if you want it to pull from your site colors.

The Query field is for those who know how to query a google spreadsheet and need something custom.  For most installations just filling in the Page Column setting with the column that contains the URL of the page the comment came from is sufficient.  This setting allows the plugin to be used across multiple pages with each pages comments sticking with just that page and yet all of them being stored in a single document.

You must create a Google Form so that Google is ready to receive the comments and put them into the spreadsheet.  Look at the source code of the live version of the Google Form you create to find the 'action' URL from the form and put that in the Submit URL field.

The Delimited Form Rows field also comes from the source code of the Google Form.  You will need the field 'id' s from each field you want to collect in this instance of the control.  Separate the friendly name from the field id with a ":" and separate each field set with a comma ",".
FriendlyName:field_id######,Email:field_id#####,Comments:field_id######,Submit:field_id######
There are two special fields in the above setting.  The first is any friendlyname prefixed with 'Comment', these fields will be rendered as textboxes rather than input boxes.  The second is the Submit field, there can only be one of these fields, and the field_id associated with it must be the id of the field in which you want the page URL to be stored, it will be rendered as a hidden field.