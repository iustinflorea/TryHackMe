
Core Offensive Security Terms
Red Teaming: A structured, authorized attack methodology that simulates a real adversary to test the effectiveness of defenses and find vulnerabilities within a defined scope
Penetration Test: A structured security assessment where an authorized tester attempts to identify and exploit vulnerabilities within a defined scope to understand real-world risk
Vulnerability: A weakness or flaw in a system, application, or configuration that an attacker could abuse
Exploit: A technique or method used to take advantage of a vulnerability to achieve a specific outcome, such as accessing restricted functionality or data
Scope: The boundaries of what is allowed to be tested during an engagement. Scope defines which systems, applications, and actions are permitted, and what is off-limit


Beginning Your Assessment

Remember, Mike has asked you to assess his web application and spot any weaknesses. There are several strategies you could use to approach this assessment, but let's begin by identifying any hidden pages that shouldn't be accessible to the public. Let's test out the pages below by adding them at the end of the http://www.onlineshop.thm/ URL in the address bar. Note that upon testing a URL that does not exist, you will see an Error 404 response on the screen, indicating that the requested page cannot be found. See if you can find the hidden page now!

sitemap Use the browser to check if http://www.onlineshop.thm/sitemap exists
mail Continue checking for the remaining pages
register
login
admin


Using Automated Tools

That approach worked great, and you should have been able to identify the hidden page successfully. Entering URLs manually is not a big deal if you have a limited number of pages to test, but what if you have a long list of potential pages? One tool in an ethical hacker's arsenal is Gobuster. This tool runs in the terminal and automates the scanning for web pages. Head to the terminal in the bottom half of your split-screen view and enter the following command.

gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt

Note: To obtain a successful scan result, ensure your input matches the syntax provided above.

The command above is made up of the following parts:

gobuster The command-line tool used to perform the discovery of web content
dir Specifies the directory and file enumeration mode, which attempts to discover hidden directories and files on a web server
--url http://www.onlineshop.thm/ Sets the target website that Gobuster will scan
-w /usr/share/wordlists/dirbuster/directory-list.txt Specifies the wordlist Gobuster will use to guess directory and file names
