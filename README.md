Summary:
The ADUsers-MoveOU PowerShell script reads a list of user accounts from a file named sams.txt and moves them to a specified Organizational Unit (OU) in Active Directory.

The script starts by defining the target OU using the variable $targetOU. The Get-Content cmdlet is then used to read the contents of the sams.txt file, which contains a list of SamAccountNames for the user accounts to be moved.

For each SamAccountName in the list, the script uses a ForEach-Object loop and the Try-Catch block to attempt to move the user account to the target OU. If the operation is successful, the script updates the Result property of the $result object to OK, and if an error occurs, it updates the Result property with an error message.

Finally, the $result object is exported to a CSV file named moved.csv using the Export-Csv cmdlet.

Overall, the script provides an efficient way to move multiple user accounts from one OU to another in Active Directory.
