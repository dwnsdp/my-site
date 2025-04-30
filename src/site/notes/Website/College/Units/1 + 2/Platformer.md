---
{"dg-publish":true,"permalink":"/website/college/units/1-2/platformer/"}
---

## Things to consider before we get started

### GDevelop

GDevelope is an open source game engine designed to be easy to use. The open source nature means that anyone can contribute, GDevelope is always being updated based on what the community wants rather than on what is more profitable. Unfortunately its benefit of being easy to use also makes it less powerful than other engines. GDevelop is browser based and incredibly high level, the engine does not have a language and is instead node based. It does a lot of things for you but this means doing things they did not expect anyone to do are very difficult and poorly optimised, of course all this means you cannot create a triple A game for the PS5 but it is a perfect choice for a mobile game or simple flash style game, exactly like what we plan to do.

  

### Scope

Platformers are a perfect genre for this as they tend to be quite simple. Unfortunately we only have two weeks to make this game including the writing process which will take multiple days. So whatever I create has to be simple and to the strengths of the engine. A simple 2D platformer perfectly fits for this as they are exactly what the engine is built for.

![](https://lh6.googleusercontent.com/OnMuFGRE8-czdHSje73VoXATE_AoB5iycUUS76dgtfxczv2zCEykpd5AawkplrjSe5cK00_fq7OPR0Vw6f_hvaA)

### Platformers

Platformers, as the name may suggest, involve crossing platforms. We will be making a typical 2D platformer. These are the simplest games that exist, the player jumps from platform to platform trying not to fall into something deadly in the cracks, like spikes or lava. The player enters from the left and tries to get out the right through a door or arch. Some common mechanics that *spice up* the format include, but are not limited to:

- Keys that must be collected to pass a door or exit the level
    
- Coins that are optional to collect, boosting your score
    
- Jump pads that allow you to jump higher
    

## The Ideas

1. ## Arachnic Fella
    

You play as 'arachnid fellow', you must run across skyscraper roof tops without falling in the gaps or being caught by the security guard chasing you. As you are 'insect dude' you have a web shooter with a limited amount of uses per turn, and you are able to run up vertical surfaces. The end of the level is when you jump over a gap at the end to big for the guard to cross.

Mood board:

![](https://lh3.googleusercontent.com/Yh5SpY9W2SCjGNsXgNHIfNl-OR6JLt6KJz_ZoFpcz0fG_r9Et1820PPnOxwqyv6AK_tpiBNZEQzpixhpzRQhzvo)

![](https://lh3.googleusercontent.com/VtD1osZPsIXuJxYPWYHa_P4sPIKJYfu6nEnw4GbmQrXz57ndTCr1cij770Ybq3fjtBYNTC7EMfkZVmxWFd3h4z0)

## 2. Bilingual Owl

You play as a green owl with an intent to take out the family of those who refuse to learn Spanish. You run across a subway station picking up anyone who is not using the app and at the end of the level you throw them in front of a train. If you have not picked them all up when the train comes you lose.

![](https://lh5.googleusercontent.com/6nTPeg28MwtY2HcTReEgHrlzttxVN79IKrP7VYnKxOcsEIhCSDo6dg4FVZvmpzyc2RSs3_G30jcmjlnzCMX-C9A)

## Which will I do?

After some careful consideration I have decided I will be going with the Spiderm-Arachnid Fella Idea. Although the idea of a Bilingual Owl is rather amusing I feel the game would feel chaotic. Another reason is that the Spider idea would be more of a challenge allowing me to improve my skills.

## Evaluation

I first created a new project in GDevelop and added added some simple physics to the Player. I created variables for the velocity that is added onto the physics engines internal velocities every frame. These are also being decreased by 10% every frame.

When the player left clicks a ray is sent in the direction of the cursor. If it collides with hitboxes placed around the scene it stores the position it collided. Velocity is then added onto the player to move them towards the hit position and a line is drawn between the player and the position using a Shape painter. I also added invisible checkpoints that set the players respawn point. If they fall they respawn at the last checkpoint they where in. Though I later removed this and replaced it with the spawn being set whenever the play is still.

At this point as I relatively happy with my physics and I had plenty of time left, so I decided I would make the levels auto generating. I spent a while trying to create this until at some point I realised I had made flappy bird but worse. And it definitely wasn’t a platformer. So I scrapped the code for level generation and I created some hand built levels with my hitboxes. I will likely return to this idea at some point in the future as I can see how a webshooting game could, like flappy bird, be very addictive.

This still looked like a bunch of red squares splattered all over a screen though so I decided I needed to do some art.

I made a giant texture for all of the levels and imported it. It was a 4K image and I had five levels. This was not going to work. For a little bit I tried to instead split the image into the individual levels and showed them only when they where on screen. It is key to note that at this time the camera was just snapping to have the player on the far left whenever they hit a checkpoint so it seemed a good idea to have the split images. But in the end although this fixed the problem with memory usage I still needed to edit an image every time I wanted to update the image. Although this would have likely made the game look much better it was a significant time sink. So I booted up LibreSprite and split the texture, making a tilemap with all of the assets I could possibly ever need. (this is a complete lie) I definitely should have thought about this from the beginning rather than wasting my time with the giant textures as it allowed me to create levels with much more ease.

I created 5 levels with my new system with the very good intentions to make some more later, I never did get round to this but it’s the thought that counts.

At this point I spent multiple hours making [this](https://soundcloud.com/jake-mcgowan-music/arachnid-fella?si=274c8bf9ee5d49b6ae4314205f5fe6ee&utm_source=clipboard&utm_medium=text&utm_campaign=social_sharing) absolute banger but I won’t go into that.

Throughout this process I was constantly getting others around me to play with my web shooting mechanics and got feedback. In fact I would say the biggest sink of time was my need to obsessively tweak the values of my physics system.

Overall this project has gone well, and with a little more time I feel I could create a playable game, as unfortunately right now the game ends rather sharply and unexpectedly with no indication that is has in fact ended.

The game is not particularly intuitive and although (I feel) it looks polished it does not feel so. There is a constant spew of new bugs and if you miss a jump it quickly becomes obvious that you need skill and a little bit of luck that the physics engine does not decide you are going to die today. Players find themselves blaming the game, as, frankly, the game does feel like at any moment it could self combust. The physics are janky and the controls are unintuitive.

If I was to make the game again with a longer time period I probably would have used a more capable game engine such as Unity or Godot. I would, of course, use most of the time to make more levels and create a more overarching story. Or perhaps switched to an infinite runner. But I would also have spent some time trying to make the game feel more intuitive, maybe adding previews to the web shooter and an animation. Using a more accurate physics engine with linking rather than just pulling the player towards the end of the web.

If I was to do the project again with a large budget I would not have made the assets myself but rather payed for some premade assets or maybe, if the budget was large enough, commission them from an artist. Apart from this I do not feel that a budget was what got in the way of making this game but rather the time.

But did I meet my goals? I believe I did. The game is a platformer, a game in which you cross platforms. The game is based around spiderman jumping from building to building with web shooting mechanics. I did not make the wall climbing mechanic as I felt it made the game feel too easy, and, to be honest once I realised I was missing the mechanic I had already made the levels to not include this feature. Perhaps this would be another thing that would have changed if I had more time to work on the game.

  

![](https://lh6.googleusercontent.com/MtoXK0zFSn-Bm2kaqpmkfruOP9lybe-rTJD4qUkE1apsHfaw5K63q81XqNt94TaNYWyAGNEHX5alzV8i_3D05QI)

![](https://lh5.googleusercontent.com/axhZrCji-NbPOu0TlwtDw_fRZd57Yah7mksG7FLC3tW9D6z69T_wBavaNpjo9R61Cde87fDBPXaneMpk5JDnEsg)

## The Game

[![](https://lh3.googleusercontent.com/proxy/By1L2p8KQP_fTXHLsEdgSwuIALxfQhBFgYsJSD1OFtYXQdtJD-dG3nfi111yjAMOohLgh33W8Pc17EMSUt31N3FnMbYOelXDH28kQdNvbRmZhlBjZrhGEA)Arachnid Fella | Play on gd.gamesPlay Arachnid Fella on gd.games, a game created with GDevelop, the free and easy game-making app.](https://www.google.com/url?q=https%3A%2F%2Fgd.games%2Fdwnsdp%2Farachnidfella&sa=D&sntz=1&usg=AOvVaw1I9206DDss3rTtV-b0wCSP)