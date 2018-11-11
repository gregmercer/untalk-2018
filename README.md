
# Slack... more than chat
---

```
Why students use Slack?
What can Slack do beyond chat?
How do you create a Slack App?
What are the benefits of a Slack App?
```

---

## Why students use Slack?

### The Student Need Pyramid 

```
When's it Due? => Do.
Learn, 
Network, 
Eat / Sleep
```

---

## Why students use Slack?

### The 'Network' Need

Stanford students spend a lot of time **messaging** - they have a huge need to keep up with: 
> **classes**, **topics**, **projects**, 
> **people**, **groups**, 
> and **events**.

Slack helps with this by providing 'Channels' - areas where general as well as specific conversations happen.

---

## What can Slack do beyond chat?

### The 'Do' Need

With time being a precious resource, Students are always looking for **quick, and easy** ways to get **tasks done**.

Slack helps with this by providing 'Bots' - which open a short conversation and then take an action.  

---

## How do you create a Slack App?

### The UX View - Design Steps

0. Thinkout how to shape the conversation. 
1. Break the UX down into a sequence of short **filtering questions** which result in direct answers/actions. The key is **funneling** down.

---  

### The Developer's View - Coding Steps

All this works by just passing **JSON Messages** - between Slack and your Bot Server.
Using standard HTTP request/response protocol.

2. Write a Web Server - Creating endpoints that handle GET/POST requests, that handle messages and actions.

#### Messsages

```
const { createEventAdapter } = require('@slack/events-api');

const slackEvents = createEventAdapter(slack_signing_secret);

slackEvents.on('message', (event) => {

  // handle message

});
```

#### Actions

```
const { createMessageAdapter } = require('@slack/interactive-messages');

const slackActions = createMessageAdapter(slack_signing_secret);

slackActions.action('room_selection', (payload) => {  

  // handle room_selection

});
```

### The DevOp's View - Configure Steps

3. Configure your Bot 
```
a. Create a Bot in your Stanford Slack Workspace
b. Tell Slack the endpoints to call for your Bot
c. Set your Bot's Permission Scopes
d. Install your Bot in your Workspace.
```

---

## What are the benefits of a Slack App?

### The Business View - Faster Cycles

All of this can be done with a very small 'one-pizza' sized crew and the benefits to using this platform are great.

Here's what you get:
- Bots are **easy to create**, and **easy to deploy**.
- Bots are **easy to locally and remoting debug**, and **easy to update**.
####
- All of this adds up into **faster cycles**. 
  -- Learning more about Student's needs and what works best to answer those needs.

Here's what the students get:
- **Convenience**, **easy to discover**, **easy to use** - Use while chatting. Not a separate App. No set of Apps to update.
- **Quick actions**, taken from **any screen**.
