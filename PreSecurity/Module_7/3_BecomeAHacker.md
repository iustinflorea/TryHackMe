
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


Think Like a Hacker
To become a hacker, you must think like one. Hackers look beyond whether something works as intended and ask how it might be misused, combined with other behavior, or used for unauthorized access. This means thinking creatively and testing new ideas. Ethical hackers adopt this same mindset, but in a safe and authorized way. They find and prove risks before real attackers can.

Here are some key points to keep in mind as you continue your ethical hacking journey.

Ask questions: Don't assume a feature works as intended. Instead, ask “What if it doesn't?”
Test the unexpected: Try actions and inputs that the developers didn't consider
Chain small weaknesses: A tiny flaw may be harmless alone, but could be connected to create a bigger impact
Think like an adversary: Think “How would a malicious actor approach this target?”
A Valuable Target
Attackers are often interested in gaining valid credentials, such as usernames and passwords, because gaining access can unlock private areas of an application and increase their capabilities. Let’s explore what becomes accessible to an attacker once they gain entry to the private areas of an application.

Sensitive functionality: Features that perform essential actions, such as modifying data, viewing restricted content, or triggering processes that should only be available to authorized users
User data: Personal or private information belonging to users, such as names, email addresses, or account details, which attackers may steal, abuse, or sell
Administrative features: High-privilege functionality that allows attackers to manage users, change settings, or gain full control of the application if accessed
Further attack opportunities: Authenticated access can expose other vulnerabilities, allowing attackers to expand their access or move deeper into the application
In the previous task, you discovered a hidden page that allows registered users to sign in. While this page may appear harmless, exposing authentication functionality can allow attackers to attempt unauthorized access. In this task, you'll attempt to exploit this weakness by testing whether the login mechanism can be abused.
