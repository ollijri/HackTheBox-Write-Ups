![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/4282270f-461d-4336-96e0-f408f83f3f7f)

____________________________________________________________________________________________________________________ 

<details>
<summary> During our scan, which port do we find serving MySQL?   </summary>
  <p></p>

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/b3ff487f-2422-4131-bc8e-17dd14dbfa95)

```3306```

</details>

<details>
<summary> What community-developed MySQL version is the target running?  </summary>
  <p></p>
 
This was accessed using mysql. In mysql ```-h``` refers to the hostname of the IP Address. 

```-u``` refers to the username. 'root' was chosen as that is the default admin login for SQL, it also does not have a password by default.

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/3dc183ae-09ac-4bdb-80c4-d862fd42500c)

```Version MariaDB```
</details>

<details>
<summary> When using the MySQL command line client, what switch do we need to use in order to specify a login username? </summary>
  <p></p>

```-u```

</details>

<details>
<summary> Which username allows us to log into this MariaDB instance without providing a password?  </summary>

```root```

</details>

<details>
<summary> In SQL, what symbol can we use to specify within the query that we want to display everything inside a table?  </summary>
  <p></p>

In SQL, ```*``` means everything

</details>
 
<details>
<summary>  In SQL, what symbol do we need to end each query with?   </summary>
  <p></p>

 SQL statements are ended with ```;```

 </details>

<details>
<summary>  There are three databases in this MySQL instance that are common across all MySQL instances. What is the name of the fourth that's unique to this host?  </summary>
  <p></p>

 To show Databases, its as simple as typing ```SHOW DATABASES;```. You must remember the semicolon on the end or it will not work.

 ![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/d9647bfc-4301-43e9-b06c-7554a14fb865)

 ```htb``` is the unique database.

 </details>

<details>
<summary>   Submit root flag  </summary>
  <p></p>

 Starting at the top level, we have the htb database to look at

 ![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/eb34209d-c10d-45a2-933b-4765f0437de7)

to switch over to that database, we use the ```use``` command. As can now be seen below, the next command input has had an effect on the htb database.

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/592fbf67-0a97-4ef2-9408-2e273077a249)

Next, is to view the information to try to find the flag. After looking around, it was found in the config table.

![image](https://github.com/ollijri/HackTheBox-Write-Ups/assets/66912443/cc0f77f2-3630-4c17-bba0-9e7dad9b06c5)

</details>
