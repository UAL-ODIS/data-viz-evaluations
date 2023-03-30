# Data Visualization Challenge evaluations

Code for processing data visualization submissions

## Steps for use

1. Create folder for the year in the data folder (e.g. "data/2023")
2. Create an images folder inside that year folder ("data/2023/images")
3. Download information from the Google Sheet and save it as "responses.csv" in 
the data/YYYY folder. The file should have the following columns (these should 
all be included in a CSV export of the Google Form Responses sheet):
  + Timestamp
  + First Name
  + Last Name
  + Email Address
  + UA NetID
  + Phone Number
  + College
  + Department/Unit
  + Student Level
  + Title
  + Abstract
  + Attach static file
  + Link to additional information
  + Agree to license terms
  + Publication in UA Research Data Repository
  + Certification of Submission
  + How did you hear about the Data Visualization Challenge?
5. On Google Drive, make a folder in this year's challenge called "Evaluations"
and create a folder inside Evaluations called "Images". Copy the following 
documents from the prior year's folder (and remove the "Copy of" prefix):
  + Results
  + Image links IGNORE
  + Evaluations
4. Make a copy of each image file and rename using the first two letters of the 
first name and first two letters of the last name (Bob Sanchez = BoSa.png). Put 
these images in the Evaluations/images folder on Google Drive.
5. In the Image links IGNORE file, open the script editor (Extensions > Apps
Script). There should be one script (Data Viz Evals); update the folder ID in 
the call to `DriveApp.getFolderById()`. Note this ID will be the URL ID for the
folder, _not_ the share link ID. Save the script (Save Project) and run (may be
prompted for authorization, which is OK). Instructions for this approach are at [https://webapps.stackexchange.com/questions/88769/get-share-link-of-multiple-files-in-google-drive-to-put-in-spreadsheet](https://webapps.stackexchange.com/questions/88769/get-share-link-of-multiple-files-in-google-drive-to-put-in-spreadsheet)
6. In a spreadsheets editor, open the data/YYYY/responses.csv. Paste the links 
to image files from (5) into the "Attach static file" column. **Double-check** 
to make sure the right images line up with the right person. It helps to sort 
by first, then last name and (temporarily) paste the abbreviated file name into
the file. This replaces the link to the original file.
7. Download the renamed image files into the local data/YYYY/images folder.
8. Update the value for `eval_year` in prepare-evaluations.R and run this 
script.
9. Upload the resulting pdf (output/YYYY/Entries.pdf) to the Evaluations folder 
on Google Drive.
10. Use output/YYYY/evaluations.csv to update the Evaluations Google Sheet with
this year's participants' abbreviated names.