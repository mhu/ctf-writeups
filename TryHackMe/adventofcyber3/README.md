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
