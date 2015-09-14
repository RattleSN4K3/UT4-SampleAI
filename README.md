SampleAI
---
A test game mode with a server-sided plugin for bot logic

# Introduction

This is a minimal game type which illustrates how a C++ plugin can be used for server-sided logic, in this case the bog logic. The C++ plugin is fully optional for clients. Clients won't need to install the plugin. The server needs to have the game type installed (Blueprint pak files) and the back-end (C++ code plugin).

The C++ back-end can be found here:  
https://github.com/RattleSN4K3/SampleAIBackend

# Usage

The game modes comes in two parts. One is a back-end which is used for the bot logic and the other parts is the actual game type done with Blueprint. The Blueprint game type is referencing the C++ _BotClass_ to be used for spawning bots in the game. If the specific class is not found, the local player (or server log) would state to install the C++ plugin.

## Installation

- Download the [release](https://github.com/RattleSN4K3/SampleAIBackend/releases/latest) or compile the [source of the C++ back-end](https://github.com/RattleSN4K3/SampleAIBackend/archive/master.zip)
- Download the [latest source files](/../../archive/master.zip) of the Blueprint assets
- Extract the archive into the content folder of your editor  
`\UnrealTournamentEditor\UnrealTournament\Content`

## Packaging

Use the package script just like you do for any other mutator. The clients will download the pak file automatically (if the setup for the server/hud is correctly done). The server-sided C++ plugin is only required for the server or if the mod is used locally/offline.

The following structure should be used:
- UnrealTournament\Content\Paks\PAKFILE.pak
- UnrealTournament\Plugins\PLUGINNAME\PLUGINNAME.plugin
- UnrealTournament\Plugins\PLUGINNAME\Binaries\PLATFORM\BINARYFILE

# License
Available under [the MIT license](http://opensource.org/licenses/mit-license.php).

# Author
RattleSN4K3
