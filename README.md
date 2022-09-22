# Syndio QA Dashboard Assignment

 This repo is for the QA takehome assignment given by Syndio.

 Files with extension .odt are the bug reports, Test Run.ods is the test run for the application.
 - Use Microsoft Word or similar programs to open .odt files
 - Use Microsoft Excel or similar programs to open .ods files

## Potential Improvements

 If I had to further improve the testing methodology I would automate most of the manual E2E validations in Python. The main logic of my scripts would start by sending a GET request to the three APIs "Group Names & IDs", "Group by Function", and "Group by Role".

 - Store and parse the labels and IDs from "Group Names & IDs" JSON response. Values can be stored via dict or tuple. Then using Selenium library the script would interact with the dropdown. After the dropdown expands the script parses through the html for labels. At this point, dropdown functionality can also be tested: upon clicking on any option in the dropdown, the URL should append the correct group id in the URL.

 - On the Syndio dashboard, using a script, click on the dropdown and choose "Group by Function". Then store and parse the labels and values from the gender and race keys in "Group by Function" JSON response. Similar as above, click on Gender tab and then parse the "demographicsTab" class in the html for the different strings used. Compare with the store JSON response for validation. Click on the Race tab and repeat validation process. Back on the Syndio dashboard click on the dropdown again and choose "Group by Role". Repeat the rest of the process.        

I believe CSS elements can also be validated via scripting as well but I'm not too familiar with this beyond using Python for basic image recognition.

