# metaCore
MetaCore can be used to manage the meta platform from the UI of the NEEO remote.

Visit this page to learn more about meta: https://github.com/jac459/meta

metaCore can be used to:
- Manage the "Driver Library" of meta:
  - download/ update drivers created by the meta community to your system
  - activate/ deactivate drivers
  - reset drivers to factory default by deleting datastore files.
- Browse all "Recipes" of your NEEO system:
  - execute all actions of your installed devices
- Manage "Global Settings" of meta:
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
a) If you have followed the instructions for setting up meta, the driver file "metaCore.json" was automatically downloaded to the sub folder "./active" of your meta installation.

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

#### Manage the "Driver Library" of meta (UNDER CONSTRUCTION):
- download/ update drivers created by the meta community to your system
- activate/ deactivate drivers
- reset drivers to factory default by deleting datastore files.

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
Meta will be restarted when executing this action and UI will be unresponsive for about 1 minute. Restarting meta can be necessery in a number of situations.\
MetaCore will lauch the following command to restart your meta:\
```pm2 restart meta```

##### Update meta
MetaCore will lauch the following command to update your meta platform:\
```wget -qO- https://raw.githubusercontent.com/jac459/meta/Release/update.sh | . ./update.sh```

##### Update Driver Library
MetaCore will download the latest list of "easy to install" drivers from the meta community (drivers.manifest). After downloading the latest drivers.manifest metaCore will also check you local library folder, as well as the active folder to prepare information for the "Driver Library" (see above). Under normal circumstances this process is executed on each startup of metaCore and you dont need to ecxecute it manually. However for debugging it can be helpful to have this option. 
The success of this process is confirmed with "Driver Library successfully updated!" in the first line of the "Driver Library".\
Please keep in mind, that meta needs a connection to the internet to download the latest list.

For advanced users: In some rare cases meta is set up in such a way that is not connected to the internet. In this case metaCore wont be able to download the latest drivers.manifest and also metaCore wont be able to download the listed drivers. However you can still make use of the "Driver Library" as the Library can show all your local driver files in "./library" and "./active". If your meta platform is permanently disconnected from the internet you can also go the extra step an remove the drivers.manifest from the root folder of meta. Doing this will cause the "Driver Library" to only list your local files.

##### Restart Node-Red
MetaCore will lauch the following command to restart your Node-Red instance:\
```pm2 restart node-red```

##### Restart MQTT
MetaCore will lauch the following command to restart your mosquitto instance.:\
```pm2 restart mosquitto```

##### Show Results of Network Scan
Some drivers for meta rely on [mDNS](https://en.wikipedia.org/wiki/Multicast_DNS) to automatically find devices on your network. This option allows you to browse through the list of all devices meta was able to find - commonly known as the file "resultsDiscovery.json".
