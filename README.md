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
### Step 7: Building a Chatroom
1. Open VS Code and
create a` chatroom.lua` file

1. In chatroom.lua put : 
```lua
Members = Members or {}
```

1. Save the chatroom.lua file

1.  Load the Chatroom into aos :
```lua
.load chatroom.lua
```
1. Creating chat room with functionalities: 

Add following code in chatroom.lua:

```lua
  Handlers.add(
    "Register",
    Handlers.utils.hasMatchingTag("Action", "Register"),
    function (msg)
      table.insert(Members, msg.From)
      Handlers.utils.reply("registered")(msg)
    end
  )
```

1. Save and reload in aos : 
```lua
.load chatroom.lua
```
Check if everything works correctly with this command : 
    ```shell
Handlers.list
```
- Registering ourselves to the chatroom :

```shell
 Send({ Target = ao.id, Action = "Register" })
```

-  Add the following code to the chatroom.lua file :

```shell
  Handlers.add(
    "Broadcast",
    Handlers.utils.hasMatchingTag("Action", "Broadcast"),
    function (msg)
      for _, recipient in ipairs(Members) do
        ao.send({Target = recipient, Data = msg.Data})
      end
      Handlers.utils.reply("Broadcasted.")(msg)
    end
  )
```
- Save and reload :  

```shell
.load chatroom.lua
```
- Test : 
```shell
  Send({Target = ao.id, Action = "Broadcast", Data = "Hi!!" })
```
-  Inviting Morpheus to the Chatroom : 

Type in the aos cli and then enter : 

```shell
Morpheus = "P2RS2VtQ4XtYEvAXYDulEA9pCBCIRpJDcakTR9aW434"
```
- Send Morpheus an invitation to join the chatroom : 
```shell
Send({ Target = Morpheus, Action = "Join" })
```

- Write `Members `in aos and enter, If successful, you'll receive a broadcasted message from Morpheus.
- Inviting Trinity to the Chatroom :

Type in the aos cli and then enter : 
Trinity = "id in message"

- Invite Trinity to the chatroom : 
```shell
Send({ Target = Trinity, Action = "Join" })
```
### Step 8: Creating a token

- Create token.lua file and put : 

```lua
local bint = require('.bint')(256)
local ao = require('ao')
--[[
  This module implements the ao Standard Token Specification.

  Terms:
    Sender: the wallet or Process that sent the Message

  It will first initialize the internal state, and then attach handlers,
    according to the ao Standard Token Spec API:

    - Info(): return the token parameters, like Name, Ticker, Logo, and Denomination

    - Balance(Target?: string): return the token balance of the Target. If Target is not provided, the Sender
        is assumed to be the Target

    - Balances(): return the token balance of all participants

    - Transfer(Target: string, Quantity: number): if the Sender has a sufficient balance, send the specified Quantity
        to the Target. It will also issue a Credit-Notice to the Target and a Debit-Notice to the Sender

    - Mint(Quantity: number): if the Sender matches the Process Owner, then mint the desired Quantity of tokens, adding
        them the Processes' balance
]]
--
local json = require('json')

--[[
     Initialize State

     ao.id is equal to the Process.Id
   ]]
--
if not Balances then Balances = { [ao.id] = tostring(bint(10000 * 1e12)) } end

if Name ~= 'Test Coin' then Name = 'Test Coin' end

if Ticker ~= 'Test' then Ticker = 'Test' end

if Denomination ~= 12 then Denomination = 12 end

if not Logo then Logo = 'SBCCXwwecBlDqRLUjb8dYABExTJXLieawf7m2aBJ-KY' end

--[[
     Add handlers for each incoming Action defined by the ao Standard Token Specification
   ]]
--

--[[
     Info
   ]]
--
Handlers.add('info', Handlers.utils.hasMatchingTag('Action', 'Info'), function(msg)
  ao.send({
    Target = msg.From,
    Name = Name,
    Ticker = Ticker,
    Logo = Logo,
    Denomination = tostring(Denomination)
  })
end)

--[[
     Balance
   ]]
--
Handlers.add('balance', Handlers.utils.hasMatchingTag('Action', 'Balance'), function(msg)
  local bal = '0'

  -- If not Target is provided, then return the Senders balance
  if (msg.Tags.Target and Balances[msg.Tags.Target]) then
    bal = Balances[msg.Tags.Target]
  elseif Balances[msg.From] then
    bal = Balances[msg.From]
  end

  ao.send({
    Target = msg.From,
    Balance = bal,
    Ticker = Ticker,
    Account = msg.Tags.Target or msg.From,
    Data = bal
  })
end)

--[[
     Balances
   ]]
--
Handlers.add('balances', Handlers.utils.hasMatchingTag('Action', 'Balances'),
  function(msg) ao.send({ Target = msg.From, Data = json.encode(Balances) }) end)

--[[
     Transfer
   ]]
--
Handlers.add('transfer', Handlers.utils.hasMatchingTag('Action', 'Transfer'), function(msg)
  assert(type(msg.Recipient) == 'string', 'Recipient is required!')
  assert(type(msg.Quantity) == 'string', 'Quantity is required!')
  assert(bint.__lt(0, bint(msg.Quantity)), 'Quantity must be greater than 0')

  if not Balances[msg.From] then Balances[msg.From] = "0" end
  if not Balances[msg.Recipient] then Balances[msg.Recipient] = "0" end

  local qty = bint(msg.Quantity)
  local balance = bint(Balances[msg.From])
  if bint.__le(qty, balance) then
    Balances[msg.From] = tostring(bint.__sub(balance, qty))
    Balances[msg.Recipient] = tostring(bint.__add(Balances[msg.Recipient], qty))

    --[[
         Only send the notifications to the Sender and Recipient
         if the Cast tag is not set on the Transfer message
       ]]
    --
    if not msg.Cast then
      -- Send Debit-Notice to the Sender
      ao.send({
        Target = msg.From,
        Action = 'Debit-Notice',
        Recipient = msg.Recipient,
        Quantity = tostring(qty),
        Data = Colors.gray .. "You transferred " .. Colors.blue .. msg.Quantity .. Colors.gray .. " to " .. Colors.green .. msg.Recipient .. Colors.reset
      })
      -- Send Credit-Notice to the Recipient
      ao.send({
        Target = msg.Recipient,
        Action = 'Credit-Notice',
        Sender = msg.From,
        Quantity = tostring(qty),
        Data = Colors.gray .. "You received " .. Colors.blue .. msg.Quantity .. Colors.gray .. " from " .. Colors.green .. msg.Recipient .. Colors.reset
      })
    end
  else
    ao.send({
      Target = msg.From,
      Action = 'Transfer-Error',
      ['Message-Id'] = msg.Id,
      Error = 'Insufficient Balance!'
    })
  end
end)

--[[
    Mint
   ]]
--
Handlers.add('mint', Handlers.utils.hasMatchingTag('Action', 'Mint'), function (msg)
  assert(type(msg.Quantity) == 'string', 'Quantity is required!')
  assert(bint.__lt(0, msg.Quantity), 'Quantity must be greater than zero!')

  if not Balances[ao.id] then Balances[ao.id] = "0" end

  if msg.From == ao.id then
    -- Add tokens to the token pool, according to Quantity
    Balances[msg.From] = tostring(bint.__add(Balances[Owner], msg.Quantity))
    ao.send({
      Target = msg.From,
      Data = Colors.gray .. "Successfully minted " .. Colors.blue .. msg.Quantity .. Colors.reset
    })
  else
    ao.send({
      Target = msg.From,
      Action = 'Mint-Error',
      ['Message-Id'] = msg.Id,
      Error = 'Only the Process Owner can mint new ' .. Ticker .. ' tokens!'
    })
  end
end)
```
- Save and reload :
```shell
.load token.lua
```

- Send Trinity 1000 tokens : 
```shell
Send({ Target = ao.id, Action = "Transfer", Recipient = Trinity, Quantity = "1000"})
```
- Replace Broadcast Handler in chatroom.lua by : 

```lua
Handlers.add(
    "Broadcast",
    Handlers.utils.hasMatchingTag("Action", "Broadcast"),
    function(m)
        if Balances[m.From] == nil or tonumber(Balances[m.From]) < 1 then
            print("UNAUTH REQ: " .. m.From)
            return
        end
        local type = m.Type or "Normal"
        print("Broadcasting message from " .. m.From .. ". Content: " .. m.Data)
        for i = 1, #Members, 1 do
            ao.send({
                Target = Members[i],
                Action = "Broadcasted",
                Broadcaster = m.From,
                Data = m.Data
            })
        end
    end
)
```
- Save and reload :
```shell
.load chatroom.lua
```
- Say "It is done" : 
```shell
Send({ Target = ao.id , Action = "Broadcast", Data = "It is done" })
```
```shell
Inbox[#Inbox].Data 
```
- Claim reward : 

```shell
Send({Target = "Lz8WE41Ou1RbAiu5Ghm7_xLzVIylYM3iy8A7C6sJraY", Action = "Claim", Name = "Begin" })
Send({ Target = "Sa0iBLPNyJQrwpTTG-tWLQU-1QeUAJA73DdxGGiKoJc", Action = "Balance" })
```

```shell
.load-blueprint chat
```

```shell
.load-blueprint credUtils
CRED = "Sa0iBLPNyJQrwpTTG-tWLQU-1QeUAJA73DdxGGiKoJc"
CRED
CRED.balance  #Display  Your CRED balance has not been checked yet. Updating now. 
# CRED Balance updated: 500.000
```
- Transfer CRED in your Arconnect wallet : 

```shell
Send({ Target = "Sa0iBLPNyJQrwpTTG-tWLQU-1QeUAJA73DdxGGiKoJc", Action = "Balance" })

Send({ Target = "Sa0iBLPNyJQrwpTTG-tWLQU-1QeUAJA73DdxGGiKoJc", Action = "your_address_here", Recipient = "walletAdress", Quantity = "500000"})
```

if you completed the task for Quest 1 and If after updating you dont see the CRED after 24hrs, fill out this form here: https://forms.gle/BLJvBk2wQ6sjT1Sy5

