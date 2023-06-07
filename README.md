# Oak Valley Dairy - Business Intelligence Dashboard

This purpose of this web app is to be a starting point for a reporting dashboard for Oak Valley Dairy.  Initially, it will provide a report of the payroll cost of 100 weight of milk.

The app will need a user login - currently all users will have access to everything - there may be different user types down the road.  Users will be able to upload csv files of payroll data and milk production on a regular basis.  When they import CSV files, the data will be added to the database - duplicate records should be checked, to reduce the chance of a user importing the data twice.

On the report view(s), a user should be able to filter by date range and also select the "classes" that are included in the report.

In the csv file for milk data, the class for the milk barns are labeled: Milk Barn 1, Milk Barn 4 & Milk Barn 5 -- In the csv file for payroll, the class for the milk barns are labeled: Barn 1, Barn 4 & Barn 5 --Can we have this correlation made in the backend, so that end users don't have to manually update the csv file with matching classes before uploading?

The payroll date is the date paid - In order to populate the report correctly, we need the payroll date to be the last day of the pay period - which is the 15th of the month and the last day of the month.  In the datastudio report, we just created a field of the payroll date and subtracted 6 days, so that the date landed in the correct payroll period.  There may be a better way to make this work.

In the payroll data, the payroll amount is a negative - in order to make the report in datastudio display correctly, we had to manually remove the negative before importing into the spreadsheet.  There is likely a way to make this work on the backend, so that the spreadsheet doesn't need to be manually updated before importing.

The milk data report has several lines that are summed up - those lines don't have a scale ticket or date should be skipped on import (don't import them) - can we do that so that we don't have to manipulate the data before importing?
