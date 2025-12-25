# Web Application Penetration Testing: Command Injection Lab.

## Project overview
: This project demonstrates the discovery and exploitation of a Command Injection Vulnerability within a web application environment (DVWA). The goal was to achieve Remote Code Execution (RCE) and perform post-exploitation reconnaissance.

## How the attack works
: * The flaw: The website has tool that pings an IP address, but it lets a user add extra hidden commands using a semicolon ";".
  * Gaining access: I typed "127.0.0.1; whoami" and the website told me it's secret user account name. "www-data". This proves I can run my own commands.
  * Stealing data: I used the command "cat /etc/passwd" to see the private list of all users on the server.
  * Exploring the server: I used "ls -la" to see all the files and folders inside the website.

# What i learned
: * Websites must never trust waht a user types.
  * Programmers must use "allw-lists" to keep the site safe.
  * This shows why Command Injection is a very dangerous vulnerability.
