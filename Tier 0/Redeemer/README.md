![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/3ffa195d-04da-430a-a614-96f25010cd88)


Which TCP port is open on the machine? 

a normal nmap scan doesn not pick it up. scanning all ports though does. use the ```-p-``` flag with ```-T5``` for maximum aggression (or it will take FOREVER) to get this:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/517ae032-61d1-45fb-9acd-04f3afacaf40)

Which service is running on the port that is open on the machine? 

can use the -A flag to gather more information about the service:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/34b1b56e-a0f4-48d8-a2bb-a46134e95a64)

```redis```

What type of database is Redis? 

```In-memory Database```

Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments. 

```redis-cli```

Which flag is used with the Redis command-line utility to specify the hostname? 

```-h```

Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server? 

```info```

What is the version of the Redis server being used on the target machine? 

Referring back to the aggressive scan from before...

```5.0.7```

Which command is used to select the desired database in Redis? 

```select```

How many keys are present inside the database with index 0? 

you can connect to a remote redis server using the following syntax:

```redis-cli -h [IP ADDRESS] -p [PORT]```

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/fcb48786-e782-405a-9ee8-46aeba28bd5f)

By using the command "info" we can find the information we need at the botton of the output

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/e91be7b2-234d-4648-afa7-7375fa74105a)

```4```

Which command is used to obtain all the keys in a database? 

```KEYS *```

Submit root flag 

KEYS * can be used to print the keys, the one called flag can be safed using ```get```

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/bede0ace-c993-4043-b86e-ea53662b7c79)

