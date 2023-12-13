# Topics to Learn
1. [Domain](https://www.youtube.com/watch?v=H2al7-l1p6c)
2. [TLD](https://www.cloudflare.com/learning/dns/top-level-domain/) / [CCTLD](https://en.m.wikipedia.org/wiki/Country_code_top-level_domain)
3. [Registry](https://en.m.wikipedia.org/wiki/Domain_name_registry)
4. [Registrar](https://www.cloudflare.com/learning/dns/glossary/what-is-a-domain-name-registrar/)
5. [DNS](https://www.youtube.com/watch?v=pl2JKLbjOTM) or [refer this](https://www.cloudflare.com/learning/dns/what-is-dns/) 
6. Types of hosting - shared, VPS, dedicated, etc
7. [Email Hosting](https://www.namecheap.com/guru-guides/what-is-email-hosting/)
8. [Web Hosting](https://www.namecheap.com/hosting/what-is-web-hosting-definition/)
9. [Web Server](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server) (Apache, Nginx, IIS, etc...)
10. [Web Space](https://www.ntchosting.com/encyclopedia/internet/web-space/)
11. [Database](https://www.geeksforgeeks.org/what-is-database/)
12. [FTP](https://www.google.com/amp/s/www.geeksforgeeks.org/file-transfer-protocol-ftp-in-application-layer/amp/)
13. [Http](https://en.wikipedia.org/wiki/HTTP) / [Https](https://en.m.wikipedia.org/wiki/HTTPS)
14. Email clients (outlook, webmail, thunderbird, etc..)
15. [POP](https://www.javatpoint.com/pop-protocol), [IMAP](https://www.google.com/amp/s/www.geeksforgeeks.org/internet-message-access-protocol-imap/amp/), [SMTP](https://www.google.com/amp/s/www.geeksforgeeks.org/simple-mail-transfer-protocol-smtp/amp/)
16. [SSH](https://www.cloudflare.com/learning/access-management/what-is-ssh/)
17. Website
18. [MS SQL](https://www.tutorialspoint.com/ms_sql_server/index.htm)
19. [MySql](https://www.w3schools.com/MySQL/default.asp)
20. [cPanel](https://en.m.wikipedia.org/wiki/CPanel)
21. [Plesk](https://en.m.wikipedia.org/wiki/Plesk)
22. Spam & Anti Spam
23. [CWP](https://www.inmotionhosting.com/support/edu/control-web-panel/what-is-control-web-panel-cwp/#:~:text=Control%20Web%20Panel%20(CWP)%2C,%2Dline%20interface%20(CLI).)
24. [Cron](https://www.hostinger.in/tutorials/cron-job) for easy calculation of time use [this](https://crontab.guru)
25. [S3 Bucket](https://www.techtarget.com/searchaws/definition/AWS-bucket) 
26. [dig Command](https://www.geeksforgeeks.org/dig-command-in-linux-with-examples/) 
27. [nmap Command](https://www.geeksforgeeks.org/nmap-command-in-linux-with-examples/) 
28. [SSL Certificate](https://www.cloudflare.com/learning/ssl/what-is-an-ssl-certificate/) 
29. [Postfix](https://phoenixnap.com/kb/postfix-smtp#:~:text=Postfix%20is%20a%20free%2C%20open,service%20solution%20for%20Linux%20servers.)
30. [Hypervisor and its types](https://www.vmware.com/in/topics/glossary/content/hypervisor.html#:~:text=A%20hypervisor%2C%20also%20known%20as,such%20as%20memory%20and%20processing.)
31. [SPF record](https://www.cloudflare.com/learning/dns/dns-records/dns-spf-record/)
32. [DKIM record](https://www.cloudflare.com/learning/dns/dns-records/dns-dkim-record/)
33. [DMARC record](https://www.cloudflare.com/learning/dns/dns-records/dns-dmarc-record/)
34. [TXT record](https://www.cloudflare.com/learning/dns/dns-records/dns-txt-record/)
35. 
# Script to remove Welcome Screen From Contabo Servers 
#WelcomeScript

Cent OS 7

```
rm -rf /etc/motd && touch /etc/motd | echo -e 'LANG=en_US.utf-8\nLC_ALL=en_US.utf-8' | sudo tee -a /etc/environment && exit
```

Ubuntu

```
rm -rf /etc/motd && touch /etc/motd && touch .hushlogin && exit
```

# Cpanel to Cpanel Backup
#Cpanel_to_Cpanel

[How to Backup Website Files in cPanel](https://youtu.be/Km2o6-ML1eA)

Visit this [site](https://www.inmotionhosting.com/support/edu/cpanel/cpanel-backups/) for more detailed explanation

[How to Schedule cPanel Backups in WHM](https://youtu.be/-aYD2oDQlyU)

Visit this [site](https://www.inmotionhosting.com/support/website/setup-scheduled-cpanel-backups/) for more detailed explanation

This can also be done with the help of script by making this script and executing it onto the server (Experimental!! 😬😬)

```
#!/bin/bash
  

# Configuration

source_cpanel_user="root"

source_cpanel_ip="source_cpanel_ip"

source_backup_dir="/home/source_cpanel_user/backups"

destination_cpanel_ip="destination_cpanel_ip"

destination_cpanel_user="destination_cpanel_user"

destination_backup_dir="/home/destination_cpanel_user/backups"

  
# Generate cPanel Backup

/usr/local/cpanel/bin/backup --force
  

# Transfer Backup to Destination Server

scp ${source_backup_dir}/backup*.tar.gz ${destination_cpanel_user}@${destination_cpanel_ip}:${destination_backup_dir}/
```

# Installing Cpanel Onto Cent OS 7


# MySQL Master Slave 
#masterslave

References :
https://youtu.be/JXDuVypcHNA

https://www.digitalocean.com/community/tutorials/how-to-set-up-replication-in-mysql#step-4-retrieving-binary-log-coordinates-from-the-source

https://hevodata.com/learn/mysql-master-slave-replication/#:~:text=load%20data%20procedure.-,What%20Is%20Master%20Slave%20Replication%3F,the%20database%20all%20the%20time.

https://chat.openai.com/share/f413d3c7-ab08-4405-8997-8d011b0aefd7

https://blog.devgenius.io/setup-master-slave-replication-with-mysql-e528dcd3b24a
# Rsync
https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories

https://www.tecmint.com/rsync-local-remote-file-synchronization-commands/

https://superuser.com/questions/1349358/rsync-with-cron-job-every-minute-issue

# Issues with their solution

>
Site down: Reboot/CWP reboot/Migrate
>
SMPT: Clear postfix if sender is same block from CWP user panel
>
Account Bandwidth issue increase this form (increase disk quota and Suspended: bandwidth by appending a 0 at the end -1 to make it Infinite ) Packages -> Edit Package
