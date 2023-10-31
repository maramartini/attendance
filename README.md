# attendance

Operating Procedure for [Attendance chatbot]

Introduction:
The Attendance chatbot allows Shodo employees to log their attendance. The initial message will consist of emojis, 
and the second message will be a weekly list with a count of people present or potentially present for each day from Monday to Friday.

Users will be able to update their attendance.

In the chat, you will see a single block of responses, along with the last message from the previous week to maintain a history. 
You can use the command /newweek to view the dates of the current week and this message will never be automatically deleted.


Installation and Configuration:
To use the bot, you need to create the following:

An application in Slack.
Two slash commands: /attendance and /newweek.
Enable the following Bot Token Scopes in OAuth and permissions: channels:history, channels:read, chat:write, commands, groups:history, groups:read, im:history, mpim:history, mpim:read, users:read.
In User Token Scopes, enable: channels:history, channels:read, groups:history, groups:read, im:history, mpim:history, mpim:read.
Enable Events and subscribe to bot events: message.im.

You need to enter the URL (appending /slackevents at the end) in Events and Slash commands.

In the code, you need to include the signing secret, which can be found in Basic Information, 
and the Bot User OAuth Token, which is located in OAuth and Permissions.

Finally, in the Slack workspace, you need to retrieve the channel ID to display channel information.
