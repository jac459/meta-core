# metaCore
MetaCore allows you to manage your meta platform from your NEEO remote.

Visit this page to learn more about meta: https://github.com/jac459/meta

metaCore will allow you to:
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

## How to install meta-core
MetaCore is a "virtual device" that needs to be installed to the NEEO system.

#### Download the driver file "metaCore.json"
a) If you have followed the instructions for setting up meta, the driver file "metaCore.json" was automatically downloaded to the sub folder "./active" of your meta installation.

b) If you have a custom installation you can download the file manually:\
```wget https://raw.githubusercontent.com/jac459/meta-core/main/metaCore.json -O ~/meta/active/metaCore.json```
Meta need to be restarted after downloading the file. If you are running meta in pm2 the command is:\
```pm2 restart meta```

#### Install
Now metaCore need to be installed as a device to your NEEO system. For this use the App or the WebUI and go to:
1. Add Device and search for "meta"
2. select "JAC459 .meta2 metaCore" and click "next"
3. metaCore

| 1.      | 2.      | 3.      |
|---------|---------|---------|
| ![add1] | ![add2] | ![add3] |

| 4.      | 5.      | 6.      |
|---------|---------|---------|
| ![add4] | ![add5] | ![add6] |

[add1]:https://user-images.githubusercontent.com/39094775/159162538-da3f33ef-e9c5-4376-a665-cbf816fde6a6.png
[add2]:https://user-images.githubusercontent.com/39094775/159162573-c619273b-3f6a-4bec-927d-554c3aa99572.png
[add3]:https://user-images.githubusercontent.com/39094775/159162593-34595913-94c7-4937-b28a-3d8e2f252670.png
[add4]:https://user-images.githubusercontent.com/39094775/159162648-8fe729e5-f7ba-42cf-96c0-653687d51b5c.png
[add5]:https://user-images.githubusercontent.com/39094775/159162769-6d7fad5d-af39-4450-beb9-3c12bc5e90ab.png
[add6]:https://user-images.githubusercontent.com/39094775/159162773-946a8e24-c876-4c58-9378-89a5842f2933.png

