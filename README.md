# AWS_Black_List_Automate
The lambda function which check the IP adress on the black list and block it in Security Group 

Overview
This AWS Lambda function is written in Python and designed to check whether a given IP address is listed in a predefined blacklist. It can be used as part of a cybersecurity automation workflow to detect and respond to potentially malicious IP addresses.

Functionality
The function receives an event containing an IP address and compares it against a hardcoded list of blacklisted IPs. It returns a message indicating whether the IP is considered safe or suspicious.

Setup Instructions
Go to the AWS Lambda Console.
Create a new function using Python 3.9 or later. 
Paste the function code into the editor.
Click Deploy to save changes.
Use the Test feature to simulate input and view results. (test file in another file in this repository)

Security Notes
The blacklist is hardcoded and should be updated regularly or replaced with a dynamic source (e.g., from an external API or database).
This function does not block IPs or modify AWS resources. It only performs a check. For automated blocking, consider integrating with EC2 Security Groups or AWS Network ACLs.

What we can do more? 
Integrate with AWS GuardDuty or CloudWatch for real-time threat detection.
Add support for dynamic IP lists from threat intelligence feeds.
Trigger automated actions (e.g., block IP, send alert) based on detection.
