---
# General Setup 
This repository contains payloads that can be used on a Raspberry Pi Pico using Circuit Python. These payloads can also be used for Hak5 Rubber Ducky's but you'll need to encode the payload instead.

- For help installing Circuit Python [Click Here](https://github.com/dbisu/pico-ducky)
- For the official Hak5 Rubber Ducky Payloads [Click Here](https://github.com/hak5/usbrubberducky-payloads)
- To encode a Ducky script [Click Here](https://ducktoolkit.com/)
- For help with the Ducky language [Click Here](https://docs.hak5.org/hc/en-us/articles/360010555153-Ducky-Script-the-USB-Rubber-Ducky-language)

---

# Disable Anti Virus (AV)
**Summary:** This payload is intended to be added to other payloads that you write. Most of the time you'll need to disable anti virus prior to being able to run any additional payloads. This method also doesn't use Powershell/Command Prompt which helps make it less detectable.

**Setup:** Copy the code in **Disable_AV_payload.dd** to the beginning of your payload

**Note:** Delays may need to be adjusted to ensure payload runs smoothly

---

# Reverse Shell
Credit: [hak5.org](https://docs.hak5.org/hc/en-us/articles/360010555233-How-to-Get-a-Reverse-Shell-in-3-Seconds-with-the-USB-Rubber-Ducky)

**Summary:** This payloads sets up a reverse shell on the target machine and allows for additional payloads/commands to be executed at a later date.

**Setup:** In order to get a reverse shell you will need the **Reverse-Shell_payload.dd** and **rspayload.ps1** files:
- First, the **rspayload.ps1** file should be hosted online either on a web server or on GitHub (what I recommend)
- In this file, you'll need to update the IP to your attacking machine and the Port to your listeners port
- Then you'll need to update **Reverse-Shell_pyload.dd** on line 34 to reflect where you are hosting the **rspayload.ps1** file
- See the file **Reverse_Shell_Commands.txt** for example commands you can run once you have a reverse shell set up
---

# Windows Wallpaper Changer
**Summary:** This payload does as the name would suggest. It downloads an image from the internet using Chrome. Saves it to the users "Downloads" folder and sets the background to that photo. Once complete it locks the screen to surprising the victim once they log in again.

**Setup:** Change the URL after "chrome.exe" in the file **ChangeWallpaper_payload.dd** to a photo of your choice and you'll be all set.

---
# Wifi Password Stealer
**Summary:** This payload opens up a small powershell window and executes commands to dump wifi profiles (including passwords), email the wifi dump file, and deletes the created file to avoide later detection.

**Setup:** In the **Wifi_Password_Stealer_payload.dd** file you'll need to change the following information
- $Recipient
- $Sender
- $Password
- $Subject
- $Body

After updating this information you should be able to run the script on the target machine.

---
# Python Script Generator
**Summary:** This payload disables AV and creates a Python script that will be automatically run on startup. This can be used to create and run various scripts such as a Python keylogger.

**Setup:** In the **Script_Generator_payload.dd** file you'll need to...
- Change the filename from **Python-Script.py** to whatever name you want
- Add your script after the **-Value** flag on line 40
  - Note: Your script will need to be on one line with ';' after each command

I've added the file **Keylogger_payload.dd** as an example of how to write your scripts. For instructions/code for this keylogger please see [this](https://github.com/TylerPaplham/Python-Projects)

---
**Disclaimer:** These payloads are for education purposes only! I'm not responsible for any unethical use of my code.




