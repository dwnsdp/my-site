---
{"dg-publish":true,"permalink":"/website/college/units/1-2/final-evaluation/"}
---

I set out to perfectly replicate a Camera that the college had. But that did not quite happen, and I'll tell you why.

Though at first I was making sure to perfectly align the references I soon realised this to be an impossible goal without a perfectly isometric image as things that are further away seem smaller.

For the body I chose to make a basic hard model before remeshing and sculpting as the body had an organic shape. This worked well or most parts but for more geometric parts I had to use boleans to cut parts out before adding a hard mesh, this made the scene very full. Also, sculpting meant I needed an absurd polycount and decimation only resulted in a messy mesh, or remeshing would have remove key details. Over all this technique was *fine* but I may want to find something better in the future.

All of the little details such as buttons went smoothly as I just made primitives and snapped to the body, although at this point I had basically began to ignore the reference. But the lens is another story. Due to a mistake splitting the cylinder to be able to animate it I ended up with a very funky mesh. At some point I decided I wanted a functional lens, but this was practically impossible. The curved surfaces needed so many subdivisions as well as it being glass that the render would have taken over an hour for one image, and I would need multiple images in order to be able to focus the lens. The optics are still in there, but they will likely never see the light of day.

I quite enjoyed making the materials. (except for the screen which I will talk about in a moment) most of the materials are just basic Principled BSDFs with noise acting as bump / roughness maps. However the screen was a different story as I had put it somewhere in my head that I would like to simulate an LCD. This was easy enough so I decided I would like the screen to display what the camera could see. This was not a good idea as I do not exactly understand vectors in the slightest and ray portals were needed. When I eventually got the portal working well enough I needed to integrate it with the LCD, and that is where I hit an unpassable roadblock. Ray portals only work in cycles but in order to convert the portal to rgb and apply effects to it I needed Eevee, In the end I chose Eevee as I wanted a relatively quick render and so all of my maths was scrapped. This was probably not the smartest series of events, in the future I will think before I come up with something quite so undoable.

The animation quite a fun process. At first I wanted it to be rendered through a mirror so that the camera was filming itself. But after trying for awhile I decided this was a bad idea as I could not monitor the animation without raytracing. So I decided to play a camera so that it looked like it was through a mirror, and added a plane with smudges to sell the effect, but it was not convincing in the slightest. I kind of kept the premise with the lens zooming in as the camera zoomed, but this was not obviously what was happening, in the future I would probably find a concept for animation that did not require such trickery.

But this was not the only thing that went wrong with the animation. There was a certain point where I could not make the animation smooth enough and I resorted to baking the frames and applying a smooth function. This made the animation smooth enough but now that the keys are baked I have no way of changed locations of the camera.

In the end making the camera was a learning experience. I was not really able to accurately model the camera as as my ideas got more dramatic I began to forget the original goal. If I did this again I would probably focus less on the impressive looking render and more on the task at hand; recreating the camera accurately.

If I was to do this project again with more time I would have spent longer in the reference stage and rather than sculpting a vague shape of the camera I would have hard surface modelled. Another thing that would be different is that rather than using poorly made procedural textures I would have captured the texture of the real thing. If I had more time I also would have been able to create an environment for the camera to be in rather than floating in an endless void.

If I was to do this project again with a large budget I would have purchased assets for the textures, and I would have been a lot more careful about sticking to the goal.

  

We decided to recreate [this scene](https://www.youtube.com/watch?v=wxL8bVJhXCM) featuring darth vader from the end of rogue one in a sweded style.

We first created a plan of the props that we would need and wrote a risk assessment using the colleges default form to make sure what we were doing was safe. Darth Vader was easy to make as someone had a helmet and someone else, a light sabre. The troopers where just people in bike helmets, the card machine as piece of cardboard with a slot cut in it, the card itself a student ID and the beginning and opening shots simply drawing on a piece of paper.

We then went through the shots, in no particular order ticking items off a list, and attempted to recreate them. I was on the camera and having a great time. As I did not have a tripod or anything fancy we results to some peculiar measures as I used an office chair as a dolly, speeding down the corridor. People seemed to enjoy infiltrating our set, but for the most part when actually filming the process was quite easy. For the final shot we needed to be outside and as such had to walk through college with Darth and a lightsaber. As one stranger put it; "what the f**k is wrong with you"

Once we had the clips I started cutting them loosely together in premier, using the original clip is reference. Although I don't have much experience in the program this was relatively easy and after a *cinematic* colour grade we had done the video.

But we didn't have any audio yet. We recorded most of the sounds in a quite room in college but at some point we needed more and the room was occupied. Fortunately lifts are very noise insulated and sound dampening. We recorded all of the music and audio after the fact (including dialogue as the actually filming location was to loud) and after I had lined it up in premier we got this *beautiful* final result.

The most difficult part of this project was attempting to organise and motivate the actors. We likely could have finished much more quickly if we had a committed team.

If we were to do this project again with a longer time period we would have been more careful about accuracy. We probably would have found locations that more closely represented the scenes. However I feel that making the project too accurate would probably remove some of the watchability. If the film was a perfect recreation there would be no need to recreate and it would lose it’s humour. I we could do this project again with a longer time period not a lot would have realistically changed. We may have filmed with better equipment but the charm and rushed feeling would still need to be there.

  
  

Now let’s move onto my game development project.

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

  

At the end of the day there are two problems that are consistent for all three projects. A lack of time, and my lack of caring for sticking to my original goal. Time being the more major of these projects.