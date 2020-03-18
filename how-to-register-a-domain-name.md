# How to Set Up a Domain Name

**Update (April 24, 2019):** If you are receiving emails from GitHub regarding "outdated IP addresses" this document has now been updated to account for this change.

Registering a domain name is required for the final project.

Students with a valid .edu address can obtain a free! domain name from [Namecheap](https://nc.me/).

This document walks through the process of registering a domain name and linking it to a GitHub repository set to host static web pages.

1. Log in to CaneLink and find your `umail.miami.edu` address. This e-mail address is automatically generated when you become a student; it is what you receive before a personalized alias is created. Under "Personal Information" click "Update E-mail Address". Take note of the "preferred e-mail address" — it should end with `umail.miami.edu`. Use this e-mail address when registering with Namecheap for your domain.

2. Visit [Namecheap.com](http://namecheap.com). Create an account. Use your `umiami.edu` address during the registration process.

3. Visit [nc.me](http://nc.me), Namecheap's student registration page and choose a domain. For a professional portfolio, it is best to register something which identifies you, such as your first and last name or first initial and last name (i.e. johnsmith.me, jsmith.me).

4. Go through the registration process. When you reach the step where you are asked to select GitHub Pages or About.me, select GitHub pages.

5. After this selection, the page may appear to hang and not advance to the next step. If this happens, visit your GitHub account. You may see a new repository which did not exist previously; it has been created by Namecheap. If this repository exists, disregard the hanging page and move on to the next step.

6. Return to [Namecheap.com](http://namecheap.com). Log in.

7. Click "Domain List" in the menu on the left side of the page.

8. Next to your domain name, click the "Manage" button.

9. Click "Advanced DNS" in the menu bar.

10. If you set up your domain to use GitHub, your "A record" settings should match the detail below. You will only need to change your "CNAME record" (remember username is your GitHub username). Be sure to SAVE the records by clicking the green checkmark on the far right of each record.


| Type     | Host | Value              | TTL    |
|----------|------|--------------------|--------|
| A Record | @    | 185.199.108.153    | 30 min |
| A Record | @    | 185.199.109.153    | 30 min |
| A Record | @    | 185.199.110.153    | 30 min |
| A Record | @    | 185.199.111.153    | 30 min |
| CNAME    | www  | username.github.io | 30 min |


Open Atom and type *your* domain name (do not start it with www; i.e. `domain.com`) in a plain text file. Save this as `CNAME` (not CNAME.txt or CNAME.html -- just `CNAME`).

Add the CNAME file to the `username.github.io` repository on your computer, commit it and push it to GitHub.

**DO NOT VISIT THE DOMAIN NAME YOU JUST REGISTERED.** See below for instructions on testing your new domain.


### If you registered a domain name elsewhere

You may have a acquired domain name from a different registrar. Since it is impossible to know every registrar's setup, you may need to read the registrar's documentation to change your domain record so it points to your GitHub repository.

Ultimately, you need to provide the registrar with two "A" records and a "CNAME" record, which should be as follows (where username is your username).
Type 	Host 	Value

| Type     | Host | Value              | TTL    |
|----------|------|--------------------|--------|
| A Record | @    | 185.199.108.153    | 30 min |
| A Record | @    | 185.199.109.153    | 30 min |
| A Record | @    | 185.199.110.153    | 30 min |
| A Record | @    | 185.199.111.153    | 30 min |
| CNAME    | www  | username.github.io | 30 min |

Open Atom and type *your* domain name (do not start it with www; i.e. `domain.com`) in a plain text file. Save this as `CNAME` (not CNAME.txt or CNAME.html -- just `CNAME`).

Add the CNAME file to the `username.github.io` repository on your computer, commit it and push it to GitHub.

**DO NOT VISIT THE DOMAIN NAME YOU JUST REGISTERED.** See below for instructions on testing your new domain.


### Testing your domain

There is a very long explanation as to why you should not do this. Fixing the problem involves using the command line / terminal to delete hidden files on your computer. A very computer-savvy person could probably handle this with ease, but if this is not you, just do not visit your domain name.

When your DNS (registrar) records are updated and you have pushed a `CNAME` file to the GitHub repository where your web site is stored, visit `username.github.io` (where username is your username).

If everything has been set up correctly, you will see the URL bar of the browser change from a github.io domain to your domain!

If you receive a 404 (File Not Found) error: This is because you do not have an `index.html` file. (Remember, a server always looks for `index.html` if no file is specified as being part of the URL.) Look for another file which you know exists in the repository (perhaps `resume.html` from a previous project).
