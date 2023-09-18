# Perform SQL Injection against an SQL Database enabled web application

First, we perform an nmap scan to find the open and available ports and their services.
Nmap will scan the most common 1000 TCP ports for active services.

We are going to use super-user privilieges to run the command below with the script scanning (-sC) or version detection (-sV) flags.
Because -sC and -sV are more intrusive methods of scanning the target.

-sC: Performs a script scan using the default set of scrpts.\
-sV: Enables version detection, will detect what version are running on what port.

IP Address : 10.129.92.22

![1](https://github.com/ggouw/internal-security-audi/assets/120260071/cbf31de1-956f-4c22-a39a-914e76625b45)

![2](https://github.com/ggouw/internal-security-audi/assets/120260071/3f0c6666-1cb4-4ff2-86e3-a5399b6ae148)

The only open port we detect is port 80 TCP, running the Apache httpd 2.4.38 ((Debian))

Apache HTTP server is one of the most popular HTTP servers. It's a free and open-source application that runs web pages on either physical or virtual web servers.

In order to further specify the service running on port 80, We are going to enter the IP address directly to our browser.

![3](https://github.com/ggouw/internal-security-audi/assets/120260071/be572925-549b-48d0-83d2-351cbe1e089c)

The next step would be to test the log-in form for a possible SQL Injection vulnerability.

We could try the most common combinations in the username and passowrd fields, such as:
<li> admin : admin </li>
<li> guest : guest </li>
<li> user : user </li>
<li> root : root </li>
<li> administrator : password

For PHP languange, after the # symbol, everything turns into a comment.\
This symbol is vulnerable to SQL injection attacks, through the log-in form on the web page. it can bypass the log-in altogether.

Now we will try to performed SQL injection and find the flag.

![4](https://github.com/ggouw/internal-security-audi/assets/120260071/1b94763f-a7ec-45e2-8e06-b56de6fbfd27)

![5](https://github.com/ggouw/internal-security-audi/assets/120260071/e640c0e9-7002-48e0-a8d0-e8c427262ec3)

We successfully performed a primary SQL injection and capture the flag.


