# Mac Installation guide
This is a camper bot installation guide for macos users.
### Requirements
Create a folder (e.g. CamperBot) on your desktop and place the following items inside
<ol>
  <li>chromedriver - version 90 can be downloaded from https://chromedriver.storage.googleapis.com/index.html?path=90.0.4430.24/</li>
  <li>.pyc file - file received from email/ whatsapp/ telegram</li>
</ol>

## Step 1: Install Python
Download and install Python 3.8.8 https://www.python.org/downloads/release/python-388/
<br>
<br>
Open up a terminal window (click on the search icon :mag: on the top right of your screen and search for "terminal"). Enter the following commands to check if your installation is successful
```sh
Example-MacBook-Pro:~ username$ python3 --version
Python 3.8.8
```

```sh
Example-MacBook-Pro:~ username$ pip3 --version
pip 20.2.3 from ...
```
>For those who already have multiple versions of python installed see the section below on installing python using pyenv

## Step 2: Install Packages
Using the same terminal window, enter the following commands line-by-line to install the required packages
```sh
Example-MacBook-Pro:~ username$ pip3 install selenium

Example-MacBook-Pro:~ username$ pip3 install tqdm

Example-MacBook-Pro:~ username$ pip3 install requests
```

## Step 3: Start the Bot
On your Desktop, right click on the created folder (e.g. CamperBot) and click on the option at the bottom "New Terminal Tab at Folder"
<br>
<br>
On the new terminal tab, enter the following command to start the bot. Remember to change the filename
```sh
Example-MacBook-Pro:CamperBot username$ python3 <insert filename here>.pyc
```
>If the "New Terminal Tab at Folder" option is missing, please refer to this guide https://www.techrepublic.com/article/how-to-open-a-new-terminal-window-from-any-folder-shortcut/.
<br>

---

## Installing python with pyenv
For those who already have another version of python installed, you will either need to delete your old python version and reinstall version 3.8.8 or use **pyenv** to manage and install multiple versions of python. The pyenv install guide can be found here https://opensource.com/article/19/5/python-3-default-mac
<br>
<br>
Install Homebrew
```sh
Example-MacBook-Pro:~ username$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install pyenv
```sh
Example-MacBook-Pro:~ username$ brew install pyenv
🍺  /usr/local/Cellar/pyenv/1.2.10: 634 files, 2.4MB
```

Install python 3.8.8
```sh
Example-MacBook-Pro:~ username$ pyenv install -v 3.8.8
python-build: use openssl 1.0 from homebrew
python-build: use readline from homebrew
Downloading Python-3.8.8.tar.xz...
-> https://www.python.org/ftp/python/3.7.3/Python-3.8.8.tar.xz
Installing Python-3.8.8...
## further output not included ##
```

Set the global python version to 3.8.8
```sh
Example-MacBook-Pro:~ username$ pyenv global 3.8.8
```

Update ~/.bash-profile
```bash
Example-MacBook-Pro:~ username$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
```

Test if your installation is successful
```sh
Example-MacBook-Pro:~ username$ pyenv version
3.8.8 (set by /Users/username/.pyenv/version)
Example-MacBook-Pro:~ username$ python --version
Python 3.8.8
```
>You can now continue with steps 2 and 3 as shown above
