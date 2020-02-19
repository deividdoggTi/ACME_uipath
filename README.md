# UiPathCertificationExam

UiPath Certification Practical Exam

In this exercise, you will create a UiPath automation that performs the steps below. To achieve this, you will use the REFrameWork as the starting template and follow the UiPath development best practices.

Here are the steps performed by the Robot:

Log in to https://www.acme-test.com.
On the landing page, Dashboard, click or hover over the Vendors menu item and then click on Search for Vendor. Click on Display All Vendors. Scrape the data from the whole table displayed. The resulting datatable will be used as the input data for the process. Navigate back to the dashboard. Note: Navigation can be achieved in multiple ways by the robot - choose whichever you find best.
For each Tax ID:
Navigate to Vendors - Search page (click or hover over the Vendors menu item and then click on Search for Vendor);
Type the Tax ID into the Vendor Tax ID field;
Click on Search;
Extract the values for the Vendor, City and Country and compare them with the values from the previously extracted table from the Display All Vendors page (check for EXACT match for all fields!);
If the values are not matching, this should be categorized as a Business Rule Exception;
If the Country does NOT belong to the group {""France"", ""Russia"", ""Italy""}, this should be categorized as the second Business Rule Exception. We can only process requests from these countries. Check the Country value extracted after the individual Tax ID search;
If no Business Rule Exception, Append the resulting datatable from each page into an CSV file; you shouldn't worry about the headers and format of the output file.
Constraints to follow in the development, using the REFrameWork:

TransactionItem datatype should be a DataRow. The process should recover and retry 2 times in case of errors in navigation between the Vendor Search and Vendor Search Results pages. One transaction is the action of navigating to the Vendor Search page, searching for the TaxID and scraping the values from the resulting one row table. (Similar to ACME Process 5 from the UiPath Academy).
Create a separate workflow file for the Login to ACME. File input arguments: URL ; Username ; Password .
Create a separate workflow file for closing ACME.
Add the ACME_URL and ACME_Credential to the Excel Config file.
Populate InitAllApplications.xaml from the Framework folder with Invoking the Login to ACME and navigation to the Work Items.
Populate CloseAllApplications.xaml from the Framework folder with Invoking the Close ACME.
Populate KillAllProcesses.xaml from the Framework folder with killing the process used.
Populate the Process.xaml file with the following actions: Navigation, Searching for TaxID, Scraping, Checking if the values match, Checking for the correct Country, Appending to CSV.
Important Note: Don't use external file references outside of the project folder (including Orchestrator Assets). Place all the used files within the project folder, zip that folder and upload it to the UiPath Certification Platform.

Zip ALL the used workflow files AND the output Excel file. Then upload the .zip file to the UiPath Certification Platform.
 
Good luck!
