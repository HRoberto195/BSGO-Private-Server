# BSGO Private Server

<p align="center">
  <img width="460" height="300" src="https://vignette.wikia.nocookie.net/bsgoguide/images/2/2f/BGO_Logo_Glow.png/revision/latest?cb=20140128015211">
</p>

#### None of the repo, the tool, nor the repo owner is affiliated with, or sponsored or authorized by, BigPoint or its affiliates.
##### This server is for learning more about C# and Networking. I am not responsible for other people's Forks.
###### Feel free to open Issues or do Pull requests.

## About
BSGO Private Server is a server revival of a Massive Multiplayer Online game known as Battlestar Galactica Online that was created by BigPoint. This is an emulation of the original server, that tries to bring back the original essence of the game. It is written in C# (.NET Core 3.0) and uses MongoDB to save the player data. It still is in its initial stages so bugs and missing protocols are expected when using it.

## Features
- Supported version:
  - Latest released by BigPoint. I'm not sure if it works for other versions.
- What's working:
  - Select a faction.
  - Customize your character.
  - Load into the game.
  - Move around Alpha Ceti.
  - Choose which settings you want and have them saved when you restart the game.
  - Dock and Undock.
- What comes next:
  - Nothing as I won't really by working on this anymore.
- Known bugs:
  - There are no collisions (expected).
  - There's no tutorial scene (expected).
  - There are no missions, skills, shop items etc (expected).
  - There's a placeholder on the ranking system (expected).
  - All ships have 15s FTL time (expected).
  - After a FTL jump or join the game, you are visible for about ~1 sec and then changes into invisible.
  - Cylon/Colonial OP doesn't keep spanwed on the sector after you jump/dock but the OP icon is on the Veil Map (expected).
  - Not all ships are playable (expected as their coding isn't finished).
  - There is a problem with the ShipShop where you can't click on other ships.
  - Squads are broken (expected).
  - Chat doesn't work (expected).
  
## Usage

#### Requeriments
- Visual Studio 2019. (Optional)
- .NET Core 3.0+. (Required)
- MongoDB (https://www.mongodb.com/download-center/community). (Required)
- Battlestar Galactica Online files. (Required)
  
### How to use
#### First Time
- Add the following directory to your PATH:
> %PathToYourMongoFolder%\Server\4.2\bin
- Create the following directory:
> C:\data\db

#### Then you should be able to do the following without repeating the previous steps:
- Open a cmd and run the Mongo Daemon:
##### x64 // 64 bits
> mongod
##### x86 // 32 bits (--args are only required for the first time)
> mongod --storageEngine=mmapv1 --dbpath C:\data\db

### Since the implementation of Github Actions, you can either choose compile the server or just download a release from the Releases page

#### Compiling the server
- Compile and run the server using Visual Studio 2019.

#### Using the release
- Extract the server files
- Open a CMD and run the following command on the same folder you extracted the files:
> dotnet BSGO\ Server.dll

#### Openning the game
- Open a CMD in your BSGO/client/live folder and run:
> bsgo.exe +projectID 547 +userID 5085935 +sessionID c7faac2379e35f6404eced5f484210ba +trackingID 6cc3a6e78a753f29ccabaa0f79b7041b +gameServer 127.0.0.1 +cdn C:\Program Files (x86)\BSGO/client/live/ +language en +session b1b23d2fa2769bd59d4c1b67554599b88381afd653b156aa54cb689969ab4fb7 +version 3b27980a3b7dd77e597872106ca98000 

## Credits
- aeroson (For the implementation of UnityEngine.Quaternion).
- bubisnew.
- Mementomori (aka FLOREK BGO).

