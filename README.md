# discord.js-poll

![npm](https://img.shields.io/npm/v/discord.js-poll)
![NPM](https://img.shields.io/npm/l/discord.js-poll)
![npm](https://img.shields.io/npm/dt/discord.js-poll)

discord.js-poll is a Node.js module that allows you to create polls with your discord bot. You can customize the separator (between the title and the options) and the color of the embed.

## Installation 


```
npm i discord.js-poll
```

## Parameters type

```JavaScript
poll(message: Discord.Message, args: string[], separator: string, embedColor: Discord.ColorResolvable)
```
### Documentation 

[Discord.Message](https://discord.js.org/#/docs/main/stable/class/Message)

[Discord.ColorResolvable](https://discord.js.org/#/docs/main/stable/typedef/ColorResolvable)


## Usage example

### Code

```JavaScript
const Discord = require('discord.js');
const { poll } = require('discord.js-poll');

module.exports = {
	name: 'poll',
	description: 'Create a poll',
	usage: 'Title + Option 1 + Option 2 + Option 3 + etc',
	execute(client, message, args) {
		poll(message, args, '+', '#00D1CD');
	},
};
```

### On discord

```
!poll Is this a poll ?
```

This will return an embed message with '**Is this a poll ?**' as title and with 👍 and 👎 reactions.

![Simple Poll Image](https://cdn.discordapp.com/attachments/417731712135725066/834428865342472212/unknown.png)


```
!poll What is your favorite food ? + Pasta + Burgers + Pizza
```

This will return an embed message with '**What is your favorite food ?**' as title and '*Pasta*', '*Burger*' and '*Pizza*' as fields, with corresponding reactions (🇦 => 🇨).

(If **'+'** is chosed as separator)

![Poll Image](https://cdn.discordapp.com/attachments/417731712135725066/834428463616229456/unknown.png)

### ⚠️ You cannot add more than 26 options to the poll. 