![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/dede44c8-bc8d-4ef0-b73e-4f82988d0dbc)


What does the acronym SQL stand for? 

```Structured Query Language```

What is one of the most common type of SQL vulnerabilities? 

```SQL Injection```

What does PII stand for? 

```Personally Identifiable Information```

What is the 2021 OWASP Top 10 classification for this vulnerability? 

```A03:2021-Injection```

What does Nmap report as the service and version that are running on port 80 of the target? 

Using the "-A" flag in nmap to get more information:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/7e51f3e5-ec4d-4630-a3a5-9d02f3c0045a)

```Apache httpd 2.4.38 ((Debian))```

What is the standard port used for the HTTPS protocol? 

```443```

What is a folder called in web-application terminology? 

```directory```

What is the HTTP response code is given for 'Not Found' errors? 

```404```

Gobuster is one tool used to brute force directories on a webserver. What switch do we use with Gobuster to specify we're looking to discover directories, and not subdomains? 

```dir``` <--- toootally guessed this one!

What single character can be used to comment out the rest of a line in MySQL? 

```The "#" key```

If user input is not handled carefully, it could be interpreted as a comment. Use a comment to login as admin without knowing the password. What is the first word on the webpage returned? 

Putting the IP into the web browser brings us here:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/d5907200-772c-4188-9637-67aa40a7cded)

The username to use is ```admin'#```. The reason for this is that putting the little ' after admin closes the statement that is formed in SQL, and the comment stops SQL from then checking for a password. Internally, it is saying:

``` SELECT * FROM users WHERE username = 'admin' (everything after here is cut by the comment) ```

This will work and provide you with the flag:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/79fc9f0b-f476-4c4e-8622-03f3171ff210)
