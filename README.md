## Attention:
at the moment this readme still describes version 4 of metaCore. The changes regarding version 5 (especially in the section ["Global Settings"](https://github.com/jac459/meta-core/edit/main/README.md#global-settings)) still have to be incorporated. In the meantime, the changes can be found in the [changelog of Version 5](https://github.com/jac459/meta-core/commit/6a04a55a672c8c816bbf189b18b745a30aef2ae1). 

# metaCore
MetaCore can be used to manage the meta platform from the UI of the NEEO remote.

Visit this page to learn more about meta: https://github.com/jac459/meta

metaCore can be used to:
- Manage the ["Driver Library"](https://github.com/jac459/meta-core#manage-the-driver-library-of-meta) of meta:
  - download/ update drivers created by the meta community to your system
  - activate/ deactivate drivers
  - reset drivers to factory default by deleting datastore files.
- Browse all ["Recipes"](https://github.com/jac459/meta-core#recipes) of your NEEO system:
  - execute all actions of your installed devices
- Manage ["Global Settings"](https://github.com/jac459/meta-core#global-settings) of meta:
  - Restart meta
  - Update meta
  - Update Driver Library (Download latest Library with Drivers created by the community)
  - Restart Node-Red (Restart your Node-Red instance.)
  - Restart MQTT (Restart your mosquitto instance.)
  - Show Results of Network Scan (Browse resultsDiscovery.json)

Advanced users might run meta without the use of metaCore and know how to execute all those operations manually. For example by transfering files or by executing code on the command line. However metaCore can be used to execute all those operations from the NEEO remote in a convenient way and without further knowledge.

## How to install meta-core
MetaCore is a "virtual device" that needs to be installed to the NEEO system.

#### Download the driver file "metaCore.json"
a) If you have followed the [instructions](https://github.com/jac459/meta#b---how-to-install-meta-on-a-new-rasberry-pi-step-by-step-for-total-beginners) for setting up meta, please skip b). The driver file "metaCore.json" was automatically downloaded to the sub folder "./active" of your meta installation.

b) If you have a custom installation you can download the file manually with this command:\
```wget https://raw.githubusercontent.com/jac459/meta-core/main/metaCore.json -O ~/meta/active/metaCore.json```

Meta needs to be restarted after downloading/ moving the file to the folder "./active". If you are running meta in pm2 the command for restarting meta is:\
```pm2 restart meta```

After the restart meta will run all drivers in the folder "./active". Meaning meta will run the driver for "metaCore", hence adding support for this "virtual device" to your NEEO system.

#### Install metaCore to your NEEO system
Now metaCore needs to be installed to your NEEO system like a TV, AVR or any other device. For this use the App or the WebUI and go to:
1. "Add Device" and search for: "meta"
2. Select "JAC459 .meta2 metaCore" and click "next".
3. On the next page "metaCore" will be selected automatically. Click "next".
4. Select the room to install metaCore to. It is recommended to install metaCore to a dedicated room like "Brain Setup" which contains the devices to setup your NEEO brain (NEEO Cranium with: NEEO Brain LED on/ off, NEEO Brain reboot). You can create this room in Step 4 if you like. Cick "next" to finish the installation.

| 1.        | 2.        | 3.        | 4.        |
|-----------|-----------|-----------|-----------|
| ![add1.1] | ![add1.2] | ![add1.3] | ![add1.4] |

[add1.1]:https://user-images.githubusercontent.com/39094775/159162538-da3f33ef-e9c5-4376-a665-cbf816fde6a6.png
[add1.2]:https://user-images.githubusercontent.com/39094775/159162573-c619273b-3f6a-4bec-927d-554c3aa99572.png
[add1.3]:https://user-images.githubusercontent.com/39094775/159162593-34595913-94c7-4937-b28a-3d8e2f252670.png
[add1.4]:https://user-images.githubusercontent.com/39094775/159162648-8fe729e5-f7ba-42cf-96c0-653687d51b5c.png

#### Checking Room Setup and Recipe
After installing metaCore to your NEEO system you can:
1. Go to "Device List" to check wheter metaCore was installed to the correct room.
2. Go to "Recipes" to make sure the recipe for the device "metaCore" is active.

#### Starting metaCore for the first time
When starting the device "metaCore" for the first time, the silde will say "You can add shortcuts..." (see image 1 below). To gain access to the features of metaCore the shortcut "Settings" needs to be added. For this:
1. Use the App or the WebUI to add a shortcut to this slide.
2. Click "Add a shortcut".
3. Select "metaCore"
4. Select the Directory "Settings" to add the shortcut. And finish the process by clicking "done" in the top right corner on this page and on the next.

| 1.        | 2.        | 3.        | 4.        |
|-----------|-----------|-----------|-----------|
| ![add2.1] | ![add2.2] | ![add2.3] | ![add2.4] |

[add2.1]:https://user-images.githubusercontent.com/39094775/159336486-e32d2f30-efcd-4fa4-9ba2-c2484e12e4ba.png
[add2.2]:https://user-images.githubusercontent.com/39094775/159336601-c39ada42-226f-468b-9714-cb1370288921.png
[add2.3]:https://user-images.githubusercontent.com/39094775/159336759-edbb7217-c9fc-426d-b6a6-c214186645f8.png
[add2.4]:https://user-images.githubusercontent.com/39094775/159336880-f88f60b1-7511-4d8a-87ba-79186ac34fcc.png

With this step the installation and inatial setup is finished and metaCore is ready for useage.

## Using metaCore
As mentioned above MetaCore is a "virtual device" installed to a room (see image 1 below). For using metaCore you need start the recipe "metaCore" compared a TV, AVR or any other device. All features of metaCore are implemented into the Directory "Settings" (see image 2 below). With opening the Directory "Settings" (see image 3 below) you get access to the features of metaCore.

| 1.        | 2.        | 3.        |
|-----------|-----------|-----------|
| ![add3.1] | ![add3.2] | ![add3.3] |

[add3.1]:https://user-images.githubusercontent.com/39094775/159339695-01e83e3a-0e3b-44cd-a0a7-2f5ba1a79e59.png
[add3.2]:https://user-images.githubusercontent.com/39094775/159338394-e72cbac1-a2b3-43b2-9a52-13e9492fc231.png
[add3.3]:https://user-images.githubusercontent.com/39094775/159340136-81c38ead-6420-4399-822b-937545bc3f44.png

#### Manage the "Driver Library" of meta
The "Driver Library" can be used to manage drivers that are availabe to meta.

##### How to download, activate and run a Community Driver and how to install a related Device to the NEEO Brain
The "Driver Library" will show up a list of device drivers created by the community. These can be downloaded to your local meta system, so you can use them with your NEEO system. As an example these are instructions for managing (downloading, activating, updating) the driver "BLERC" by Nelus:

1. Open up the "Driver Library" and select a driver. In this case "BLERC" by Nelus. Note, that at this stage, the subtile of the driver is: "Available for Download".
2. The page displaying the options for this driver will pop up. The Header shows an icon, the name, the author and the driver version that is available for download.
3. First have a look at "Click here for more info and readme". This will show up a short explanation of the driver and it will point to the readme, which contians more important info. It is highly recommended to look up the readme prior to making any further steps. For example the readme might contain info that additional hardware is necessary. For "BLERC" have a look at: github.com/jac459/Meta-Blerc.
4. A driver can be downloaded to the local driver library by clicking "Download this Driver" (see image 2 below). After downloading, the same button will change to "Update this Driver" (see image 4 below), so an updated version can be downloaded later. (Or the same file can be downloaded again, if it was corrupted by the user.) Downloading a driver means, that it is "just" stored to the local library and sits there. For using a driver with you NEEO system it needs to be activated with the next steps (5-9).

| 1.        | 2.        | 3.        | 4.        |
|-----------|-----------|-----------|-----------|
| ![add4.1] | ![add4.2] | ![add4.3] | ![add4.4] |

5. Note: When a driver is available in the local library, the subtitle in the "Driver Library" will say: "Not active".
6. Activating a driver is done by clicking "Activate Driver". This will move a copy of the driver from the local library (folder: "./library") to the place with all the activated drivers (folder: "./active").
7. After clicking "Activate Driver", the status will change and subtitle in the "Driver Library" will say: ">>DRIVER ACTIVE<<". However one final step regarding meta is necessary.
8. As a final step, meta needs to be restarted to check the (new) activated drivers and initialise/ run them. This can be done using metaCore by going to: Global Settings > restart meta (see details [here](https://github.com/jac459/meta-core#restart-meta)).
9. (without image) After restarting meta, the driver will be made accessible to the NEEO brain. To finally install the device to you NEEO system, use the NEEO app or the web UI and go to "add device". Follow the instruction on the screen and the additional info provided in the related readme.

| 5.        | 6.        | 7.        | 8.        |
|-----------|-----------|-----------|-----------|
| ![add4.5] | ![add4.6] | ![add4.7] | ![add4.8] |

[add4.1]:https://user-images.githubusercontent.com/39094775/205027649-a604358e-a45b-4a11-bccf-25b7a803f3a3.png
[add4.2]:https://user-images.githubusercontent.com/39094775/205027662-7f67d218-b5d0-4e27-9a35-833b95d85d84.png
[add4.3]:https://user-images.githubusercontent.com/39094775/205027705-672da73e-35c9-437b-8b3d-3f2d740171d1.png
[add4.4]:https://user-images.githubusercontent.com/39094775/205027728-3a94dfd8-d7c0-45c3-89ca-8e88f2d783a9.png
[add4.5]:https://user-images.githubusercontent.com/39094775/205027755-ef0c296d-c3a3-45c6-9efb-1d60c654ed7e.png
[add4.6]:https://user-images.githubusercontent.com/39094775/205027769-42865e2b-5288-4bed-b420-e36bdd271eb5.png
[add4.7]:https://user-images.githubusercontent.com/39094775/205027784-8471d0ee-2e5c-4ce8-a49b-428a0b13df44.png
[add4.8]:https://user-images.githubusercontent.com/39094775/205027776-50371dc1-5b46-409f-86e6-2b456086b9ba.png

##### How to update a Community Driver
Usually driver updates are announcement on the forum. The driver version available for download can be looked up in the header of the driver page in the "Driver Library" (see image 6 above). Note: This displayed version number is NOT the version installed in the system! The version number installed in the system can be looked up in the device info of the NEEO app.

For updating a Driver:
- Click "Update this Driver". This will download the latest version of the driver to the local file system. If this is an "active" driver, updating will place a copy in the folder "./active", as well as in the folder "./library".
- As a last step meta need to be restarted. This can be done using metaCore by going to: Global Settings > restart meta (see details [here](https://github.com/jac459/meta-core#restart-meta)).
- After restarting meta, the new version number will show up in the device info of the NEEO app.

Note: Some driver updates may require uninstalling a device from the NEEO brain and reinstalling it to take effect. This information should be given on the announcement of the driver update.

##### How to deactivate a Community Driver
If a Driver for a Device is not needed anymore, it can be uninstalled and deactivated as follows:
- Uninstall the device (all instances!) using the NEEO app or the web UI.
- Using metaCore browse to the related driver and click "Deactivate Driver". This will remove the driver from the active devices (folder: "./active").
- If the driver details in metaCore show the option to "Delete DataStore" this can also be executed (see details on "DataStore" [here](https://github.com/jac459/meta-core#option-delete-datastore)).
- As a last step meta needs to be restarted. This can be done using metaCore by going to: Global Settings > restart meta (see details [here](https://github.com/jac459/meta-core#restart-meta)).

Note: Deactivating a driver will not affect the local copy in the library (folder "./library"). So the driver will remain available for later usage. At the moment metaCore does not offer a way to remove the driver file from the local library.

##### Option "Delete DataStore"
Some drivers are using a "DataStore" to permanently store settings. For example some devices require entering an ip-adress when installing to the NEEO system and other smart drivers can remember additional setting by that. This information will be stored in the DataStore, which is an additional file that is stored next to the driver in the folder: "/.active".

Attention: Drivers using a DataStore usually rely on it! Deleting the Datastore while a device is installed in your NEEO system can cause the driver to malfunction! Only delete the DataStore when it was recommended or after deactivating/ uninstalling the device!

##### Some Background info on how the "Driver Library" works
On the startup ("POWER ON") of the recipe, metaCore is downloading a lookup table of drivers created by the community. This is the "drivers.manifest". It contains several info on each driver, most importantly the download location, which usually is a github repo. But in theory the drivers.manifest can point to any location. If metaCore was able do download the latest drivers.manifest there will a confirmation for that, when opening the "Driver Library". The first line of the directory will say "Driver Library successfully updated!" (see image 1 above). Updating the "Driver Library" can also be triggered manually by: Global Settings > Update Driver Library (see details [here](https://github.com/jac459/meta-core#update-driver-library)).

If there are localy developed custom drivers in the meta system (folders: "./library" or "./active"), that are not mentioned in the drivers.manifest, metaCore will merge them into the "Driver Library". But for obvious reasons the options will be limited to activating, deactivating and deleting the DataStore. There wont be any info in "Click here for more Info and readme" and obviously no option to download the localy developed driver.

It may happen in some setups or situations, that the meta system has no connection to internet. So the latest drivers.manifest can not (or never) be downloaded (and metaCore wont be able to download drivers). In this case, the "Driver Library" will only contain the drivers in the local library of the meta system (folder: "./library"). However the "Driver Library" will be enriched with additional info from the existing/old drivers.manifest. So at least the location of the readme for a specific driver can be displayed in "Click here for more info and readme".

#### Recipes
The "Recipes" can be used to execute ALL actions of ALL devices installed on your NEEO system. This can be helpful to quickly test an action without adding a dedicated shortcut.
For Example execute the button "Party" on a streaming speaker (WX-010) in the Kitchen: 

Recipes > Kitchen > WX-010 Küche > Party

| ![add5.1] | ![add5.2] | ![add5.3] |
|-----------|-----------|-----------|

[add5.1]:https://user-images.githubusercontent.com/39094775/159522365-369fd623-28f9-4286-9008-172e0a341e7c.png
[add5.2]:https://user-images.githubusercontent.com/39094775/159522384-ad033220-2621-4748-b375-ec0dd38fe8cd.png
[add5.3]:https://user-images.githubusercontent.com/39094775/159522397-00c30a9a-c694-4552-8fbc-0b301ffe6f1d.png

#### Global Settings
The "Global Settings" of metaCore contain the following features:

| ![add6.1] |
|-----------|

[add6.1]:https://user-images.githubusercontent.com/39094775/159341310-789a0c48-0fc8-47b8-ba90-87c009e9b0ab.png

##### Restart meta
Meta will be restarted when executing this action and UI will be unresponsive for about 1 minute.\
Restarting meta can be necessery in a number of situations. For example after updating meta or after changing the state of a Driver by updating, activating or deactivating.\
MetaCore will lauch the following command in the background to restart meta:\
```pm2 restart meta```

##### Update meta
CAUTION: This will download the latest Version of meta from github to your System. A skript will be executed to replace/update all relevant Files of meta including the metaCore Driver.\
MetaCore will launch the following script in the background:\
```wget -qO- https://raw.githubusercontent.com/jac459/meta/Release/update.sh | . ./update.sh```

Meta must be restarted for the Update to take effect (refer to the option "Restart meta" which is described above).

##### Update Driver Library
MetaCore will download the latest lookup table of "easy to install" drivers from the meta community (drivers.manifest). After downloading the latest drivers.manifest, metaCore will also check you local library folder, as well as the active folder and prepare information for the "Driver Library" (for more details see [above]([https://github.com/jac459/meta-core#some-background-info-on-how-the-driver-library-works)).\
Under normal circumstances this process is executed on each startup of metaCore and you dont need to ecxecute it manually. However for debugging it can be helpful to have this option. 

Note: Please keep in mind, that meta needs a connection to the internet to download the lookup table.

##### Restart Node-Red
MetaCore will lauch the following command to restart your Node-Red instance:\
```pm2 restart node-red```

##### Restart MQTT
MetaCore will lauch the following command to restart your mosquitto instance.:\
```pm2 restart mosquitto```

##### Show Results of Network Scan
Some drivers for meta rely on [mDNS](https://en.wikipedia.org/wiki/Multicast_DNS) to automatically find devices on your network. This option allows you to browse through the list of all devices meta was able to find - commonly known as the file "resultsDiscovery.json".


## Versions
#### Version 1 (JAC459)
- First Release

#### Version 2 (JAC459)
- Update

#### Version 3 (MarkusM)
- Now automatically updating Driver Library (drivers.manifest) on each "POWER ON"
- Driver Library: Improved appearance and Feedback to the User
- Other minor Bugfixes

#### Version 4 (MarkusM)
- Recipes: Added support for multiple Brains
- Library: Changed behaviour when downloading/ updating a driver file:
  - previously: new driver file was only downloaded to the folder "./library"
  - now: new driver file is additionally copied to folder "./actice" when driver is activated
- Other minor Bugfixes

 #### Version 5 (MarkusM)
- Changed location of the file driver.manifest. This is the library with drivers created by the community. If you are running metaCore in a previous Version (Version 4 or lower) and you go to "Library" you are suggested to update metaCore. (Canged location from: github.com/jac459/meta - to: github.com/jac459/meta-core; driver.manifest)
- "Global Settings": 
   - Restarting the processes meta, mode-red and moquitto and updating meta was rearranged: For safety reasons the execution of each of these commands was moved to a sub directory.
   - New Option "Disable logging in pm2": By default all pm2 processes restarted from metaCore are now running without logging. This decision was made to reduce wear of the sd card. However, logging can be re-enabled from metaCore if required. (For developers: pm2 restart <process_id> -o "/dev/null" -e "/dev/null")
   - New Feature "Delete pm2 logs": Under certain circumstances, the log files of pm2 can take up a lot of storage space over a longer period of time. This option allows you to delete the log files of the individual processes. (For developers: pm2 flush <process_id>)
   - Removed the feature to manually "Update Driver Library". This is not needed as this is executed on each start of metaCore.
- Other minor Bugfixes
