# discord.js-poll

![npm](https://img.shields.io/npm/v/discord.js-poll)
![NPM](https://img.shields.io/npm/l/discord.js-poll)

Note: this module uses recent discord.js features and requires discord.js version 12 and Node.js 14.

discord.js-poll is a Node.js module that allows you to create polls with your discord bot. You can customize the separator (between the title and the options) and the color of the embed.

## Installation 

<br>

```
npm i discord.js-poll
```

<br>

## Parameters type

<br>

```JavaScript
poll(message: Discord.Message, args: string[], separator: string, embedColor: Discord.ColorResolvable)
```

<br>

## Usage example

<br>

### Code

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

### On discord

This will return an embed message with 'Is this a poll ?' as title and with 👍 and 👎 reactions.

```
!poll Is this a poll ?
```

This will return an embed message with 'What is your favorite food ?' as title and Pasta, Burger and Pizza as fields, with corresponding reactions (🇦 => 🇨).

(If '+' is chosed as separator)

```
!poll What is your favorite food ? + Pasta + Burgers + Pizza
```

### ⚠️ You cannot add more than 26 options to the poll. 