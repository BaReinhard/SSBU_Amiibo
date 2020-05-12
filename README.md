# SSBU_Amiibo
Just a start for the Amiibo editor 

you will need to provide your own Amiibo Keys in `key_retail.bin` for Encription and Decription to work

Each Amiibo has to be "upgraded" from the SSB format to SSBU, you should see this message in game the first time you scan a fresh Amiibo in SSBU. After the upgraded the tag is marked and the data block is reformatted to the new SSBU preserving some of the SSB data just reformatted, scaled, etc. If the Amiibo has SSBU data in the data block before the upgraded this data will be interpreted as SSB data not SSBU data.


# How To Example:
I want to create a supper SSBU Amiibo. You will need at least 2 tags (Tagmo) or somthing like the N2 Elite. One will need to be have a stock no mods Amiibo.
 1. Download the latest [Release](https://github.com/odwdinc/SSBU_Amiibo/releases), this is the recommended installation option, place this exe file in a folder you can access it easily.
 1. If starting with a legit Amiibo skip to 4
 1. Take unmodifide.bin (`something.bin`, these names are place holders for actual character names) file write to blank Amiibo tag or to N2 Elite.
 1. Load unmodifide Amiibo in SSBU in game (Note, this will perfrom an update to the Amiibo.)
 1. `Put-Away` Amiibo in SSBU in game (Note, this will save the updates to the Amiibo.)
 1. Once the Amiibo as been updated in-game use eather Tagmo or N2 Elite to get a new bin file (somthing_new.bin)
 1. Ensure your `key_retail.bin` is in the easily accessible file you placed the `ssbu_amiibo.exe` file
 1. Open the **Amiibo editor** and go to **File->Decrypt Amiibo**, and select the new bin file (somthing_new.bin).
    - If you do not see `Decrypt Amiibo` in the File dropdown, you either have no placed the `key_retail.bin` in the correct folder, or you may need to restart the `ssbu_amiibo.exe` file.
 1. Make any changes to the Amiibo then **SAVE** (Note. you can confirm the changes by reopening the save file.)
    - It is also important to note that you can only have a total 3 `slots` per amiibo, if using more than 3 `slots` the save will leave off some of the attributes you selected.
 1. Once happy with changes go to **File->Encrypt Amiibo** and save to a new bin file (somthing_mod.bin)
 1. With a blank Amiibo tag write the new bin file (somthing_mod.bin) to a tag.
    - Alternatively, you can restore this information to an existing amiibo if you are using TagMo, it is imporant to note that if you do not have a backup of your original `unmodifide.bin` file you may not be able to use your amiibo online.
 
 # Note on Tagmo Compatibility is unknown, as I do not use. 
  Tagmo will not recognize it unless you go into the settings and turn off amiibo file browser, and even still, there's an error in loading the amiibo onto the nfc sticker. it shoue still work.

# Windows 10 64 bit
  Grab the [Release](https://github.com/odwdinc/SSBU_Amiibo/releases)

# Windows build Guide

## Get python 3.? [Link](https://www.python.org/downloads/)
![Get Python](https://github.com/odwdinc/SSBU_Amiibo/blob/master/docs/Install_Python.PNG)


### Start the installer, Conferm the "Add to Path" and pick "Customize installation"
![Install Python](https://github.com/odwdinc/SSBU_Amiibo/blob/master/docs/Install_Python_2.PNG)


### Confirm "pip" and "tcl/tk"
![Install Python](https://github.com/odwdinc/SSBU_Amiibo/blob/master/docs/Install_Python_3.PNG)


### Confirm "Install for all users"
![Install Python](https://github.com/odwdinc/SSBU_Amiibo/blob/master/docs/Install_Python_4.PNG)

## Download and Install Git

### https://git-scm.com/download/win


# Run the Code

### Find copy of "KEY RETAIL MUST HAVE TO FLASH AMIIBO.zip" or other copy of "key_retail.bin"

### Copy/Extract "key_retail.bin" to folder called Amiibo

### While holding down ctrl+shift right click in the Amiibo folder to get acces to the "Open PowerShell window here"

# Install with pip (not needed if downloading the .exe release)

install to your users home directory.

```console
python -m pip install --user git+https://github.com/odwdinc/SSBU_Amiibo.git
```


### Run the UI with the command  (not needed if downloading the .exe release)

```console
$env:Path += "$env:APPDATA\Python\Python37\Scripts;"
ssbu_amiibo.exe
```

### New window will load with UI.

### Go into File menu to access "Decrypt amiibo"

![Run Code](https://github.com/odwdinc/SSBU_Amiibo/blob/master/docs/RunCode_7.PNG)

## Hex editor usage if installed with pip

```console
pyhex
```
