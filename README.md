backup-bash
===========

This is a series of three scripts written for BASH that work in tandem to manage a backup solution. They were designed for my old home setup. The three files are:
1) masterbk
2) autoexec.back
3) extback

masterbk managed both of the other scripts and was placed in the chrontab of the two hosts running the code. 

Every night, both hosts--megesphere and colossus--would use rsync to back up their files to a local NAS called The Vault. Then, once per week, the extback script was called and backed up everything on The Vault to an external hard drive. I had two of these hard drives that I would rotate, making sure that one was always off site in the case of catastrophic failure: like my apartment building burning down. You will also see calls to "mail" in the code; these scripts not only created log files, but also sent me emails through a local postfix server on colossus to tell me if they completed correctly. 

I'm making these scripts available through a github repository to provide a sample of my coding philosophy--comment, comment, comment, and meaningful error messages--but I doubt they will be useful to anyone. 
