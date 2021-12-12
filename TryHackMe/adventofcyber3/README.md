# Advent of Cyber 3 (2021)

* Link: https://tryhackme.com/room/adventofcyber3

## Day 1 - Save The Gifts

> After finding Santa's account, what is their position in the company?

**Answer**: The Boss!

> After finding McStocker's account, what is their position in the company?

**Answer**: Build Manager

> After finding the account responsible for tampering, what is their position in the company?

**Answer**: Mischief Manager

> What is the received flag when McSkidy fixes the Inventory Management System?

**Answer**: THM{AOC_IDOR_2B34BHI3}

## Day 2 - Elf HR Problems

> What is the name of the new cookie that was created for your account?

**Answer**: user-auth

> What encoding type was used for the cookie value?

**Answer**: hexadecimal

> What object format is the data of the cookie stored in?

**Answer**: JSON

> What is the value of the administrator cookie? (username = admin)

**Answer**: 7b636f6d70616e793a2022546865204265737420466573746976616c20436f6d70616e79222c206973726567697374657265643a2254727565222c20757365726e616d653a2261646d696e227d

> What team environment is not responding?

**Answer**: HR

> What team environment has a network warning?

**Answer**: Application

## Day 3 - Christmas Blackout

> Using a common wordlist for discovering content, enumerate http://10.10.124.198 to find the location of the administrator dashboard. What is the name of the folder?

**Answer**: admin

> In your web browser, try some default credentials on the newly discovered login form for the "administrator" user. What is the password?

**Answer**: administrator

> Access the admin panel. What is the value of the flag?

**Answer**: THM{ADM1N_AC3SS}

## Day 4 - Santa's Running Behind

> What valid password can you use to access the "santa" account?

**Answer**: cookie

> What is the flag in Santa's itinerary?

**Answer**: THM{SANTA_DELIVERS}

## Day 5 - Pesky Elf Forum

> What flag did you get when you disabled the plugin?

**Answer**: THM{NO_MORE_BUTTMAS}

## Day 6 - Patch Management Is Hard

> Deploy the attached VM and look around. What is the entry point for our web application?

**Answer**: err

> Use the entry point to perform `LFI` to read the `/etc/flag` file. What is the flag?

**Answer**: THM{d29e08941cf7fe41df55f1a7da6c4c06}

> Use the PHP filter technique to read the source code of the `index.php`. What is the `$flag` variable's value?

**Answer**: THM{791d43d46018a0d89361dbf60d5d9eb8}

> Now that you read the `index.php`, there is a login credential PHP file's path. Use the PHP filter technique to read its content. What are the username and password?

**Answer**: McSkidy:A0C315Aw3s0m

> Use the credentials to login into the web application. Help McSkidy to recover the server's password. What is the password of the `flag.thm.aoc` server?

**Answer**: THM{552f313b52e3c3dbf5257d8c6db7f6f1}

> The web application logs all users' requests, and only authorized users can read the log file. Use the LFI to gain RCE via the log file page. What is the hostname of the webserver? The log file location is at `./includes/logs/app_access.log`.

**Answer**: lfi-aoc-awesome-59aedca683fff9261263bb084880c965

## Day 7 - Migration Without Security

> Interact with the MongoDB server to find the flag. What is the flag?

**Answer**: THM{8814a5e6662a9763f7df23ee59d944f9}

> Can you log into the application that Grinch Enterprise controls as `admin` and retrieve the flag?

**Answer**: THM{b6b304f5d5834a4d089b570840b467a8}

> Once you are logged in, use the gift search page to list all usernames that have `guest` roles. What is the flag?

**Answer**: THM{2ec099f2d602cc4968c5267970be1326}

> Use the gift search page to perform NoSQL injection and retrieve the `mcskidy` record. What is the details record?

**Answer**: ID:6184f516ef6da50433f100f4:mcskidy:admin

## Day 8 - Santa's Bag of Toys

> What operating system is Santa's laptop running ("OS Name")?

**Answer**: Microsoft Windows 11 Pro

> What was the password set for the new "backdoor" account?

**Answer**: grinchstolechristmas

> In one of the transcription logs,  the bad actor interacts with the target under the new backdoor user account, and copies a unique file to the Desktop. Before it is copied to the Desktop, what is the full path of the original file?

**Answer**: C:\Users\santa\AppData\Local\Microsoft\Windows\UsrClass.dat

> The actor uses a Living Off The Land binary (LOLbin) to encode this file, and then verifies it succeeded by viewing the output file. What is the name of this LOLbin?

**Answer**: certutil.exe

> What specific folder name clues us in that this might be publicly accessible software hosted on a code-sharing platform?

**Answer**: .github

> Additionally, there is a unique folder named "Bag of Toys" on the Desktop! This must be where Santa prepares his collection of toys, and this is certainly sensitive data that the actor could have compromised. What is the name of the file found in this folder?

**Answer**: bag_of_toys.zip

> What is the name of the user that owns the SantaRat repository?

**Answer**: Grinchiest

> What is the name of the repository that seems especially pertinent to our investigation?

**Answer**: operation-bag-of-toys

> What is the name of the executable that installed a unique utility the actor used to collect the bag of toys?

**Answer**: uharc-cmd-install.exe

> Following this, the actor looks to have removed everything from the bag of toys, and added in new things like coal, mold, worms, and more!  What are the contents of these "malicious" files (coal, mold, and all the others)?

**Answer**: GRINCHMAS

> What is the password to the original bag_of_toys.uha archive?

**Answer**: TheGrinchiestGrinchmasOfAll

> How many original files were present in Santa's Bag of Toys?

**Answer**:228

## Day 9 - Where Is All This Data Going

> In the HTTP #1 - GET requests section, which directory is found on the web server?

**Answer**: login

> What is the username and password used in the login page in the HTTP #2 - POST section?

**Answer**: McSkidy:Christmas2021

> What is the User-Agent's name that has been sent in HTTP #2 - POST section?

**Answer**: TryHackMe-UserAgent-THM{d8ab1be969825f2c5c937aec23d55bc9}

> In the DNS section, there is a TXT DNS query. What is the flag in the message of that DNS query?

**Answer**: THM{dd63a80bf9fdd21aabbf70af7438c257}

> In the FTP section, what is the FTP login password?

**Answer**: TryH@ckM3!

> In the FTP section, what is the FTP command used to upload the secret.txt  file?

**Answer**: STOR

> In the FTP section, what is the content of the secret.txt file?

**Answer**: 123^-^321

## Day 10 - Offensive Is The Best Defence

> Help McSkidy and `run nmap -sT MACHINE_IP`. How many ports are open between 1 and 100?

**Answer**: 2

> What is the smallest port number that is open?

**Answer**: 22

> What is the service related to the highest port number you found in the first question?

**Answer**: HTTP

> Now run nmap -sS 10.10.217.4. Did you get the same results? (Y/N)

**Answer**: Y

> If you want Nmap to detect the version info of the services installed, you can use `nmap -sV 10.10.217.4`. What is the version number of the web server?

**Answer**: Apache httpd 2.4.49

> What is the CVE number of the vulnerability that was solved in version 2.4.51?

**Answer**: CVE-2021-42013

> She explains that adding `-p1-65535` or `-p-` will scan all 65,535 TCP ports instead of only scanning the 1000 most common ports. What is the port number that appeared in the results now?

**Answer**: 20212

> What is the name of the program listening on the newly discovered port?

**Answer**: telnetd

## Day 11 - Where Are The Reindeers?

> There is an open port related to MS SQL Server accessible over the network. What is the port number?

**Answer**: 1433

> If the connection is successful, you will get a prompt. What is the prompt that you have received?

**Answer**: 1>

> What is the first name of the reindeer of id 9?

**Answer**: Rudolph

> Check the table schedule. What is the destination of the trip scheduled on December 7?

**Answer**: Prague

> Check the table presents. What is the quantity available for the present “Power Bank”?

**Answer**: 25000

> There is a flag hidden in the `grinch` user's home directory. What are its contents?

**Answer**: THM{YjtKeUy2qT3v5dDH}

## Day 12 - Sharing Without Caring

> How many TCP ports are open?

**Answer**: 7

> Which port is detected by Nmap as NFS or using the mountd service?

**Answer**: 2049

> How many shares did you find?

**Answer**: 4

> How many shares show “everyone”?

**Answer**: 3

> What is the title of file 2680-0.txt?

**Answer**: Meditations

> It seems that Grinch Enterprises has forgotten their SSH keys on our system. One of the shares contains a private key used for SSH authentication (id_rsa). What is the name of the share?

**Answer**: confidential
