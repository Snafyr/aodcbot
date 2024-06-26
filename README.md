Assuming you already have aos

Step 1 : Run this command in root;
```
npm install discord.js ws @permaweb/aoconnect fs
```

Step 2 : Project Directory Structure
```
 /root/DevChat/src/
├── capture.js
├── index.js
├── process.lua
├── client.lua
├── chatroom.lua
├── router.lua
```

Step 3 : Configure index.js 

I suggest you to use VScode for this
You need to change

```
const token 'YOUR DISCORD BOT TOKEN ID'
const channelId 'YOUR DISCORD CHANNEL ID (e.g general-chat)'
await message({
    process: 'yourprocessID'
```

these parts
the other files are just fine

Step 4 : Run these commands on aos

```
.load /root/DevChat/src/router.lua
.load /root/DevChat/src/client.lua
.load /root/DevChat/src/chatroom.lua
.load /root/DevChat/src/process.lua
```

Step 5 : Register the Channel

```
ao.send({ Target = "xnkv_QpWqICyt8NpVMbfsUQciZ4wlm5DigLrfXRm8fY", Action = "Register", Name = ao.id })
```

Step 6 : Join the registered channel in the aos terminal

```
Join(ao.id)
```

Step 7 : Open 2 new screens

In one of them run ;

```
node /root/DevChat/src/index.js
```

and in the second one run ;

```
node /root/DevChat/src/capture.js
```

In total you need to have 3 screens. You can close them later.

Step 8 : Testing the Setup Sending a Message from DevChat

```
Say("Hello, this is a test message.", ao.id)
```

Check if the bot send the message to your server.

The result should look like this;

![image](https://github.com/Snafyr/aodcbot/assets/83130343/6cb72138-24ee-49c6-be66-c77be14fb612)
