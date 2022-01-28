# Scavenger Hunt

* Points: 50
* Category: Web Exploitation

## Description

> There is some interesting information hidden around this site
>
> http://mercury.picoctf.net:39698/. Can you find it?

## Solution

First we want to take a look at the source code of the website, which reveals the first part of the flag:

```html
<!-- Here's the first part of the flag: picoCTF{t -->
```

We can also see that the index.html includes two more files, mycss.css and myjs.js.

We find this in the mycss.css source code:

```css
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
```

... and this in the myjs.js source code:

```javascript
/* How can I keep Google from indexing my website? */
```

Next, we'll use gobuster to look for hidden directories and files:

```sh
gobuster dir -u http://mercury.picoctf.net:39698 -w /usr/share/wordlists/dirb/common.txt
```

Gobuster found two helpful files; robots.txt:

```txt
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```

... and .htaccess:

```
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```

This information led me to check whether information was stored in cookies or the browser's local/session storage, unsuccessfully.
Since the capitalized word in the previous hint (_Access_) was most likely hinting towards the .htaccess file, I googled for the capitalized words in this hint - _Mac_ and _Store_, until I found out that macOS uses .DS_Store files to store information about folders.

If we access http://mercury.picoctf.net:36968/.DS_Store, we see this:

```
Congrats! You completed the scavenger hunt. Part 5: _fa04427c}
```

## Flag

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_fa04427c}
