# License_Expiry_Checker_Monitoring
License_Expiry_Checker_Monitoring_and_Alerting_for_Software_Licenses
Doc:- 

License Expiry Checker: Monitoring and Alerting for Software Licenses.

•	Check the available license file expiration date.
•	Start sending mail to sys admin team and license team members on that month in which license file going to expire.
•	Sending mail sequence are: - first mail will send before 30 days and then after on start of week. 
•	In last week in which file going to expire continues sending mail till date the of expire if license file.

Algorithm of code: 
1.	Import necessary libraries:
•	Import the required Python libraries, Including:-  subprocess, os , email, smtplib, datetime.
2.	Functions we create:-
•	send_email
•	check_license_expiry_Adient 
•	get_expiry_date_command
3.	Funcations:- 
•	send_email:- Its read the license file and  attached that with mail and send it
•	check_license_expiry_Adient:-  Its read the license file and extract the vendor and check expire date with current date and also in it we define sending mail days sequences .
First mail should send 30 days before and then after every weak send a mail and in the end of date of license file expired start sending mail before 7 days.
•	get_expiry_date_command:- In it we use subprocess module to grab the license check command out the compare with it current date, and the out put of this send in send email function send a mail with name of the command of that we used to check license check.
4.	Execute the main function:
•	Call the main function with the provided path and action to initiate the script's operation.
Testing:-
30 22 * * * python /scripts/validLicense.py
