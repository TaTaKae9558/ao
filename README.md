# AO Computer

AO Computer is a highly parallel computing system designed to provide reliable and collaborative computing services that can evolve indefinitely

Key features of AO include parallel processing, unlimited computation, interaction with Arweave, autonomous processes, and modular design.

For more information read this thread https://x.com/0x_Rorschach/status/1770138088137723986?s=20

The platform enables autonomous interaction with Arweave and allows users to earn CRED, the native currency of the AO testnet, by completing community quests.

First we will try to configure our environment, Then started the first quest together.

# Getting started
**I use a vps with Ubuntu 20.04 (64 Bit). I advise you not to use your PC if you want to use it you must have Ubuntu.**

1. Installing Ubuntu 20.04

1. Server update
```shell
sudo apt update -y && sudo apt upgrade -y
```
1. Installing git
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

1.  Installing Node 20+

Installs NVM (Node Version Manager)
```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```
Download and install Node.js
```shell
nvm install 20
```
Verifies the right Node.js version is in the environment
```shell
node -v # should print `v20.*.*`
```
Verifies the right NPM version is in the environment
```shell
npm -v # should print `10.*.*`
```
1. Installing AOS

**Create a directory and place it in the directory**
- Create Directory : 
```shell
mkdir nameOfYourDirectory
```
- Go to new directory:
```shell
cd nameToYourDirectory
```
- **Install AOS** : 
```shell
npm i -g https://get_ao.g8way.io
```
After installation run the command to  start a new aos process : 
```shell
aos
```

Once you run the command you should have this :
```shell
         /\    \                 /::\    \                 /\    \
        /::\    \               /::::\    \               /::\    \
       /::::\    \             /::::::\    \             /::::\    \
      /::::::\    \           /::::::::\    \           /::::::\    \
     /:::/\:::\    \         /:::/~~\:::\    \         /:::/\:::\    \
    /:::/__\:::\    \       /:::/    \:::\    \       /:::/__\:::\    \
   /::::\   \:::\    \     /:::/    / \:::\    \      \:::\   \:::\    \
  /::::::\   \:::\    \   /:::/____/   \:::\____\   ___\:::\   \:::\    \
 /:::/\:::\   \:::\    \ |:::|    |     |:::|    | /\   \:::\   \:::\    \
/:::/  \:::\   \:::\____\|:::|____|     |:::|    |/::\   \:::\   \:::\____\
\::/    \:::\  /:::/    / \:::\    \   /:::/    / \:::\   \:::\   \::/    /
 \/____/ \:::\/:::/    /   \:::\    \ /:::/    /   \:::\   \:::\   \/____/
          \::::::/    /     \:::\    /:::/    /     \:::\   \:::\    \
           \::::/    /       \:::\__/:::/    /       \:::\   \:::\____\
           /:::/    /         \::::::::/    /         \:::\  /:::/    /
          /:::/    /           \::::::/    /           \:::\/:::/    /
         /:::/    /             \::::/    /             \::::::/    /
        /:::/    /               \::/____/               \::::/    /
        \::/    /                 ~~                      \::/    /
         \/____/                                           \/____/

ao Operating System

aos - 1.4.1
2024 - Type ".exit" to exit
aos process:  1xM1_lDZ428sJHpTX7rtcR6SrDubyRVO06JEEWs_eWo

aos>
```
**You have executed your first aos process** 

**To exit the aos process press ctrl+c**

# Quests 1: Begin

#### Do these actions on your PC before starting the quest
1. Download Arconnect, An Arweave-native wallet https://www.arconnect.io/download
**Once quest 1 is completed we will transfer the test tokens to this wallet**

1. Download and install Visual Studio Code Editor https://code.visualstudio.com/
After installation, click on extensions on the left side of the main page.

**For those who have installed the aos client on a vps**: 

- After installation, click on extensions on the left side of the main page
![image](https://github.com/ruesandora/AO/assets/101149671/126f07c3-c549-4c31-8c06-b3279c8e8ee3)


Then, we download Microsoft's plug-in by typing SSH in the search field

![image](https://github.com/ruesandora/AO/assets/101149671/b786c7ca-4003-43dd-8457-806eb3c8e237)

After our plugin is installed, we click on the >< sign at the bottom left.

![image](https://github.com/ruesandora/AO/assets/101149671/6b1e6848-2da9-44ca-b36c-4ad019a73454)

> We click on Connect to Host.

![image](https://github.com/ruesandora/AO/assets/101149671/d85744f2-4c1b-4b85-a60c-3cd0dac61f67)

> Add New SSH Host

![image](https://github.com/ruesandora/AO/assets/101149671/2ad00eee-a91e-4ada-81d8-746df7473a29)

> We enter our IP and press Enter.

> Then we click on the top option.

> We click on Open config from the notification at the bottom right.

![image](https://github.com/ruesandora/AO/assets/101149671/5330cedb-dbbd-4fb4-a441-0fe06b02ce67)


![image](https://github.com/ruesandora/AO/assets/101149671/a35ef4a0-1ee5-4bab-90b4-14b8bf9ffc6e)

> Then we click on >< at the bottom left again and click Connect to Host.

> We select our IP and enter our password.


**For everyone, install the Lua plugin: Open Addon Manager**

![image](https://github.com/ruesandora/AO/assets/101149671/63cbae39-9575-449f-a040-c86e25b05e31)

## Communication in aos CLI

### Step 1 : Open the aos CLI

To access the aos command-line interface (CLI), follow these steps:

1. Launch your terminal.
2. Type `aos` and press Enter.

```shell
aos
```

### Step 2: Sending a Message
To send a message to a specific process, use the Send function with the following format:


```shell
Send({ Target = "process ID", Data = "Hello World!" })
```

Send: This function is globally available in the aos interactive environment.
Target: Include the Target field to specify the recipient process.
Data: This represents the text message intended for the receiving process.

### Step 3:  Storing Morpheus's Process ID

You can store Morpheus's process ID as a variable for easier interaction

```shell
Morpheus = "P2RS2VtQ4XtYEvAXYDulEA9pCBCIRpJDcakTR9aW434"
```

### Step 4: Sending a Message to Morpheus
After storing Morpheus's process ID, you can communicate with him using the Send function:

```shell
Send({ Target = Morpheus, Data = "Morpheus?" })
```

### Step 5: Checking the Inbox
The Inbox is where you receive messages from other processes. To check your inbox:

sh
Copy code
```shell
#Inbox
```
To read the last message in your inbox:

```shell
Inbox[#Inbox].Data
```

### Step 6: Sending Messages with Tags
Tags in aos messages are used to categorize, route, and process messages efficiently. You can add tags to a message using the appropriate syntax.

```shell
Send({ Target = Morpheus, Data = "Code: rabbithole", Action = "Unlock" })
```






