# discord.js-poll

![npm](https://img.shields.io/npm/v/discord.js-poll)
![NPM](https://img.shields.io/npm/l/discord.js-poll)

Note: this module uses recent discord.js features and requires discord.js version 12 and Node.js 14.

discord.js-poll is a Node.js module that allows you to create polls with your discord bot. You can customize the separator (between the title and the options) and the color of the embed.

## Installation 

```
npm i discord.js-poll
```

## Usage example

```JavaScript
const Discord = require('discord.js');
const { poll } = require('discord.js-poll');

module.exports = {
	name: 'poll',
	description: 'Create a poll',
	usage: 'Title - Option 1 - Option 2 - Option 3 - etc',
	execute(client, message, args) {
		poll(message, args, '-', '#00D1CD');
	},
};
```

## Parameters type

```JavaScript
poll(message: Discord.Message, args: string[], separator: string, embedColor: Discord.ColorResolvable)
```