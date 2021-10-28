# General Setup 
This repository contains payloads that can be used on a Raspberry Pi Pico using Circuit Python. These payloads can also be used for Hak5 Rubber Ducky's but you'll need to encode the payload instead.

For help installing Circuit Python [Click Here](https://github.com/dbisu/pico-ducky)

For the official Hak5 Rubber Ducky Payloads [Click Here](https://github.com/hak5/usbrubberducky-payloads)

To encode a Ducky script [Click Here](https://ducktoolkit.com/)

For help with the Ducky language [Click Here](https://docs.hak5.org/hc/en-us/articles/360010555153-Ducky-Script-the-USB-Rubber-Ducky-language)

# Reverse Shell
Credit: [hak5.org](https://docs.hak5.org/hc/en-us/articles/360010555233-How-to-Get-a-Reverse-Shell-in-3-Seconds-with-the-USB-Rubber-Ducky)

In order to get a reverse shell you will need the **Reverse-Shell_pyload.dd** and **rspayload.ps1** files

-First, the **rspayload.ps1** file should be hosted online either on a webserver or on GitHub (what I recommend)

-In this file you'll need to update the IP to your attacking machine and the Port to your listeners port

-Then you'll need to update 'Reverse-Shell_pyload.dd' on line 34 to reflect where you are hosting the **rspayload.ps1**

-See the file 'Reverse_Shell_Commands.txt' for example commands you can run once you have a reverse shell set up
