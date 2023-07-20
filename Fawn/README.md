![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/6674402f-c390-436a-a4cd-f56a78cf572d)

What does the 3-letter acronym FTP stand for? 

```File Transfer Protocol```

Which port does the FTP service listen on usually? 

```21```

What acronym is used for the secure version of FTP? 

```sFTP```

What is the command we can use to send an ICMP echo request to test our connection to the target? 

```ping```

From your scans, what version is FTP running on the target? 

- running nmap [IP ADDRESS] with the tag "-A" to gain more info on the server

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/00907a90-f7ca-4081-a8f8-76a5ec41c7d5)

version number is visible as vsftpd 3.0.3 and it has also revealed a flag on the server too

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/b7443167-8b87-4f21-a6f2-9a18e01c581e)

From your scans, what OS type is running on the target? 

- running nmap with the "-O" tag reveals OS information

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/35315124-1f94-4c6e-8093-87c2a95bd8f4)

``` answer is unix (which linux is v similar to) ```

What is the command we need to run in order to display the 'ftp' client help menu? 

``` ftp -h```

What is username that is used over FTP when you want to log in without having an account? 

```anonymous```

What is the response code we get for the FTP message 'Login successful'? 

no password was specified in the below screenshot:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/5ca4cbaf-95d2-446f-8440-f2cbe1f9f465)

```230```

There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system. 

```ls```

There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system. 

```get```

Submit root flag 

Here I grab it from the server:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/850b8836-10f7-43fb-b1fd-b41e85352d9b)

and here it is viewing it on my pc:

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/f516f860-2593-40f6-81be-9612ee6fbb4f)
