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

> What is the MD5 sum of id_rsa?

**Answer**: 3e2d315a38f377f304f5598dc2f044de

## Day 13 - They Lost The Plan!

> Complete the username: p.....

**Answer**: pepper

> What is the OS version?

**Answer**: 10.0.17763 N/A Build 17763

> What backup service did you find running on the system?

**Answer**: IperiusSvc

> What is the path of the executable for the backup service you have identified?

**Answer**: C:\Program Files (x86)\Iperius Backup\IperiusService.exe

> Run the whoami command on the connection you have received on your attacking machine. What user do you have?

**Answer**: the-grinch-hack\thegrinch

> What is the content of the flag.txt file?

**Answer**: THM-736635221

> The Grinch forgot to delete a file where he kept notes about his schedule! Where can we find him at 5:30?

**Answer**: jazzercize

## Day 14 - Dev(Insecure)Ops

> How many pages did the dirb scan find with its default wordlist?

**Answer**: 4

> How many scripts do you see in the /home/thegrinch/scripts folder?

**Answer**: 4

> What are the five characters following $6$G in pepper's password hash?

**Answer**: ZUP42

> What is the content of the flag.txt file on the Grinch's user’s desktop?

**Answer**: DI3H4rdIsTheBestX-masMovie!

## Day 15 - The Grinchs day off

No answers needed!

## Day 16 - Ransomware Madness

> What is the operator's username?

**Answer**: GrinchWho31

> What social media platform is the username associated with?

**Answer**: Twitter

> What is the cryptographic identifier associated with the operator?

**Answer**: 1GW8QR7CWW3cpvVPGMCF5tZz4j96ncEgrVaR

> What platform is the cryptographic identifier associated with?

**Answer**: Keybase.io

> What is the bitcoin address of the operator?

**Answer**: bc1q5q2w2x6yka5gchr89988p2c8w8nquem6tndw2f

> What platform does the operator leak the bitcoin address on?

**Answer**: GitHub

> What is the operator's personal email?

**Answer**: DonteHeath21@gmail.com

> What is the operator's real name?

**Answer**: Donte Heath

## Day 17 - Elf Leaks

> What is the name of the S3 Bucket used to host the HR Website announcement?

**Answer**: images.bestfestivalcompany.com

> What is the message left in the flag.txt object from that bucket?

**Answer**: It's easy to get your elves data when you leave it so easy to find!

> What other file in that bucket looks interesting to you?

**Answer**: wp-backup.zip

> What is the AWS Access Key ID in that file?

**Answer**: AKIAQI52OJVCPZXFYAOI

> What is the AWS Account ID that access-key works for?

**Answer**: 019181489476

> What is the Username for that access-key?

**Answer**: ElfMcHR@bfc.com

> There is an EC2 Instance in this account. Under the TAGs, what is the Name of the instance?

**Answer**: HR-Portal

> What is the database password stored in Secrets Manager?

**Answer**: Winter2021!

## Day 18 - Playing With Containers

> What command will list container images stored in your local container registry?

**Answer**: docker images

> What command will allow you to save a docker image as a tar archive?

**Answer**: docker save

> What is the name of the file (including file extension) for the configuration, repository tags, and layer hash values stored in a container image?

**Answer**: manifest.json

> What is the token value you found for the bonus challenge?

**Answer**: 7095b3e9300542edadbc2dd558ac11fa

## Day 19 - Something Phishy Is Going On

> Who was the email sent to? (Answer is the email address)

**Answer**: elfmcphearson@tbfc.com

> Phishing emails use similar domains of their targets to increase the likelihood the recipient will be tricked into interacting with the email. Who does it say the email was from? (Answer is the email address)

**Answer**: customerservice@t8fc.info

> Sometimes phishing emails have a different reply-to email address. If this email was replied to, what email address will receive the email response?

**Answer**: fisher@tempmailz.grinch

> Less sophisticated phishing emails will have typos. What is the misspelled word?

**Answer**: stright

> The email contains a link that will redirect the recipient to a fraudulent website in an effort to collect credentials. What is the link to the credential harvesting website?

**Answer**: https://89xgwsnmo5.grinch/out/fishing/

> View the email source code. There is an unusual email header. What is the header and its value?

**Answer**: X-GrinchPhish: >;^)

> You received other reports of phishing attempts from other colleagues. Some of the other emails contained attachments. Open attachment.txt. What is the name of the attachment?

**Answer**: password-reset-instructions.pdf

> What is the flag in the PDF file?

**Answer**: THM{A0C_Thr33_Ph1sh1ng_An4lys!s}

## Day 20 - What's the Worst That Could Happen?

> Open the terminal and navigate to the file on the desktop named 'testfile'. Using the 'strings' command, check the strings in the file. There is only a single line of output to the 'strings' command. What is the output?

**Answer**: X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*

> Check the file type of 'testfile' using the 'file' command. What is the file type?

**Answer**: EICAR virus test files

> Calculate the file's hash and search for it on VirusTotal. When was the file first seen in the wild?

**Answer**:  2005-10-17 22:03:48

> On VirusTotal's detection tab, what is the classification assigned to the file by Microsoft?

**Answer**: Virus:DOS/EICAR_Test_File

> Go to [this link](https://www.eicar.org/?page_id=3950) to learn more about this file and what it is used for. What were the first two names of this file?

**Answer**: ducklin.htm or ducklin-html.htm

> The file has 68 characters in the start known as the known string. It can be appended with whitespace characters upto a limited number of characters. What is the maximum number of total characters that can be in the file?

**Answer**: 128

## Day 21 - Needles In Computer Stacks

> We changed the text in the string $a as shown in the eicaryara rule we wrote, from X5O to X50, that is, we replaced the letter O with the number 0. The condition for the Yara rule is $a and $b and $c and $d. If we are to only make a change to the first boolean operator in this condition, what boolean operator shall we replace the 'and' with, in order for the rule to still hit the file?

**Answer**: or

> What option is used in the Yara command in order to list down the metadata of the rules that are a hit to a file?

**Answer**: -m

> What section contains information about the author of the Yara rule?

**Answer**: metadata

> What option is used to print only rules that did not hit?

**Answer**: -n

> Change the Yara rule value for the `$a` string to `X50`. Rerun the command, but this time with the `-c` option. What is the result?

**Answer**: 0
