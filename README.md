---
# General Setup 
This repository contains payloads that can be used on a Raspberry Pi Pico using Circuit Python. These payloads can also be used for Hak5 Rubber Ducky's but you'll need to encode the payload instead.

- For help installing Circuit Python [Click Here](https://github.com/dbisu/pico-ducky)
- For the official Hak5 Rubber Ducky Payloads [Click Here](https://github.com/hak5/usbrubberducky-payloads)
- To encode a Ducky script [Click Here](https://ducktoolkit.com/)
- For help with the Ducky language [Click Here](https://docs.hak5.org/hc/en-us/articles/360010555153-Ducky-Script-the-USB-Rubber-Ducky-language)

---

# Disable Anti Virus (AV)
This payload is intended to be added to other payloads that you write. Most of the time you'll need to disable anti virus prior to being able to run any additional payloads. This method also doesn't use Powershell/Command Prompt which helps make it less detectable.

Simply copy the code in **Disable_AV_payload.dd** to the beginning of your payload

**Note:** Delays may need to be adjusted to ensure payload runs smoothly

---

# Reverse Shell
Credit: [hak5.org](https://docs.hak5.org/hc/en-us/articles/360010555233-How-to-Get-a-Reverse-Shell-in-3-Seconds-with-the-USB-Rubber-Ducky)

In order to get a reverse shell you will need the **Reverse-Shell_payload.dd** and **rspayload.ps1** files:
- First, the **rspayload.ps1** file should be hosted online either on a web server or on GitHub (what I recommend)
- In this file, you'll need to update the IP to your attacking machine and the Port to your listeners port
- Then you'll need to update **Reverse-Shell_pyload.dd** on line 34 to reflect where you are hosting the **rspayload.ps1** file
- See the file **Reverse_Shell_Commands.txt** for example commands you can run once you have a reverse shell set up
---

# Windows Wallpaper Changer
This payload does as the name would suggest. It downloads an image from the internet using Chrome. Saves it to the users "Downloads" folder and sets the background to that photo. Once complete it locks the screen to surprising the victim once they log in again.

Change the URL after "chrome.exe" in the file **ChangeWallpaper_payload.dd** to a photo of your choice and you'll be all set.

---

**Disclaimer:** These payloads are for education purposes only! I'm not responsible for any unethical use of my code.




