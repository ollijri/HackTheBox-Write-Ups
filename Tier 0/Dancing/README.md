![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/fb02a0dd-cab4-4fc7-a6f9-310d146a58dc)


What does the 3-letter acronym SMB stand for? 

```Server Message Block```

What port does SMB use to operate at? 

```445```

What is the service name for port 445 that came up in our Nmap scan? 

used nmap [IP ADDRESS]

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/0e90cd54-9e50-4e13-85b3-7070570a0bf1)

```microsoft-ds```

What is the 'flag' or 'switch' we can use with the SMB tool to 'list' the contents of the share? 

```-l```

How many shares are there on Dancing? 

on mac (my OS) you gotta use smbutil instead of smbclient

```-l``` becomes ```view``` | ```-g``` logs in as guest

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/c6eca8a9-5feb-4b8d-ab8c-f35ac0e489ba)


```4```

What is the name of the share we are able to access in the end with a blank password? 

i used finder in linux to do this as smbutil was giving me brainrot. well, whatever works!

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/302ca66f-53fb-4810-964e-2cad567b63c8)

```workshares``` is the only one available so thats the answer

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/6fe8077e-de07-4e34-8062-833b7870f233)

What is the command we can use within the SMB shell to download the files we find? 

```get```

 Submit root flag 

 I did this a lil differently as i mounted it to mac, its much nicer to look at this way. found flag in James.P > Flag.txt

 ![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/98e86a33-2691-4732-84c1-31de04a0e2e4)
