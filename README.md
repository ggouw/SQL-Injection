# Perform SQL Injection against an SQL Database enabled web application

First, we perform an nmap scan to find the open and available ports and their services.
Nmap will scan the most common 1000 TCP ports for active services.

We are going to use super-user privilieges to run the command below with the script scanning (-sC) or version detection (-sV) flags.
Because -sC and -sV are more intrusive methods of scanning the target.

-sC: Performs a script scan using the default set of scrpts.
-sV: Enables version detection, will detect what version are running on what port.

