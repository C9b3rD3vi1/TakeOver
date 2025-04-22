# TakeOver

This challenge revolves around subdomain enumeration.

Hello there,

I am the CEO and one of the co-founders of futurevera.thm. In Futurevera, we believe that the future is in space. We do a lot of space research and write blogs about it. We used to help students with space questions, but we are rebuilding our support.

Recently blackhat hackers approached us saying they could takeover and are asking us for a big ransom. Please help us to find what they can takeover.

Our website is located at https://futurevera.thm

Hint: Don't forget to add the 10.10.119.204 in /etc/hosts for futurevera.thm

## 📝 Summary

In this challenge, I gained unauthorized access to an internal support subdomain by enumerating DNS records and parsing certificate data. By chaining directory fuzzing and weak configuration logic, I achieved a web-based subdomain takeover.


## 🧰 Tools Used

    gobuster, ffuf

    openssl

    dig

    nmap

    Web browser

    /etc/hosts editing

## 🚀 Step-by-Step Walkthrough

1️⃣ Initial Recon & Setup
Downloaded and connected to the THM machine.

Added base domain to /etc/hosts:

![Add base domain to /etc/hosts](./hosts_add.png)

Verified web service running:

    http://futurevera.thm

This allow you to access the web interface of the challenge in the browser

![http://futurevera.thm](./futureVera.png)