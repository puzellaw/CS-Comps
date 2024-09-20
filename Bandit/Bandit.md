Login Info  
SSH Address: bandit.labs.overthewire.org  
Port: 2220  
Username: bandit  
Password: **go find it**  

# Level 0:
	- used ls to find readme file
	- password located in the readme 
	**password for L1: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If**
# Level 1:
	- password locate in a file named "-"
	- used `less ./-` to open file
	**password for L2: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx**
# Level 2: 
	- password was located in a file called "spaces in this filename" 
	- used `less sp*` to avoid having to include all the `\` required to open file
	**password for L3: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx**
# Level 3:
	- changed directories into "inhere"
	- used `ls -a` to find hidden file called "...Hiding-From-You"
	- openned file
	**password for L4: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ**
# Level 4:
	- changed directories into "inhere"
	- I then used `file ./*` to determine the file types of all ten files in the directory
	- found that only -file07 was text and it contained the password
	**password for L5: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw**
# Level 5:
	- changed directory into "inhere"
	- password was located in a file 1000 in size rather than 1033 
	- found it in a directory "maybehere07" 
	- found in a file ".file2"
	**password for L6: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG**
# Level 6: 
	- so I just used find to find file owned by user bandit7 and owned by the group bandit 6
	- used command `find / -user bandit7 -group bandit6 -size 33c -type f 2>/dev/null`
	- password located in the file "/var/lib/dpkg/info/bandit7.password"
	**password for L7: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj**
# Level 7:
	- Found the password in the data.txt file
	- used less to open "data.txt"
	- `/millionth` to search for the term millionth
	**password for L8: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc**
# Level 8: 
	- password was line that was unique in the data.txt file
	- used `sort data.txt | uniq -u`
	**password for L9: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM**
# Level 9:
	- looked in data.txt for string with a bunch "="
	- specifically used string command 
	- `strings data.txt | grep '='`
	**password for L10: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey**
# Level 10:
	- used base64 decode to find file in data.txt file
	- ran `base64 -d data.txt`
	**password for L11: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr**
# Level 11:
	-  used the tr command combined with cat to translate the data.txt file 13 positions
	- specifically `tr a-zA-Z n-za-mN-ZA-M` which shifts a to n...
	- `cat data.txt | tr a-zA-Z n-za-mN-ZA-M`
	**password for L11: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4**
# Level 12: 
	- made a new working tmp dir called "thisisnotthedirectoryyouarelookingfor"
	- used `xxd -r` to reverse hex dump
	- used file to determine type
	- gzip file 
	- renamed to gz and gunziped
	- file is now bzip2
	- renamed to bz2
	- bunzip2 the file
	- file is gzip again
	- renamed and gunzip again
	- now tar file
	- used `tar -xf hex` to unpack tar archive
	- file in archive is called data5.bin
	- type claims to be ascii but honestly I dont believe that still looks like last tar file
	- I was right!!
	- now the output file is a bzip2 again so rename and bunzip2
	- now its another tar
	- welcome data8.bin to the party
	- it's another gzip
	- and the password has been found in data8
	**password for L13: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn**
# Level 13:
	- Well they gave me a private sshkey so im gonna try and connect to level 14 from level 13
	- otherwise ill just copy it into my local 
	- using -i modifier to tell where key is
	- oh ya it worked
# Level 14:
	- passwords are located in /etc/bandit_pass/bandit14 which made it MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
	- used nc to query local host
	- `nc localhost 30000`
	- provided password 
	**password for L15: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo**
# Level 15:
	- made a new directory called "thisreallyisntthedirectoryyourlookingfor"
	- made a file called "password.txt" which contained the passwords from the previous levels
	- used openssl client to make connection
	- `openssl s_client -connect localhost:30001 -ign_eof < password.txt`
	- got a connected response
	**password for L16: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx**
# Level 16:

	
	
