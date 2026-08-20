# Homework assignment HW5

## Homework log

Remember to create a new post with a new topic "HW5" in your homework log channel on Microsoft Teams. Make a reply to that topic whenever do some work on this assignment. You can also post questions there. Your posts should provide evidence that you spent several hours doing meaningful work.

## Objectives

This assignment  **todo**

Minimal knowledge and experience to acquire include the following:
* install `apache2` on on your Linux system
* launch apache web server: `sudo /etc/init.d/apache2 start`
* Configure the web server so that you can visit its default page (see e.g. the [Apache on GCP](../resources/apache_gcp_quickstart.md) page).
* Edit the default page at `/var/www/html/index.html`. Don't edit the file as root user. Practice adding yourself to a group that has write access to the file, and then edit it as a normal user. 
  - Commands similar to the following should work. Make sure you understand them all:
    ```bash
        sudo groupadd www
        sudo usermod -a -G www yourusername
        cd /var/www
        sudo chgrp -R www html
        sudo chmod -R g+w html
    ```
  - The Linux machine probably needs a reboot so that the new group permissions work correctly.
* Install Docker Engine (not Docker Desktop) on the Linux box. see e.g. [Install using the convenience script](https://docs.docker.com/engine/install/debian/#install-using-the-convenience-script)



## PB version

The Professor Braught version is available as:
* [x](../materials/)

<!-- _Unless you already have familiarity with the above commands, it is a good idea to follow the PB version closely for this assignment._ -->


## Likely quiz questions

