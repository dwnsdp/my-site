---
{"dg-publish":true,"permalink":"/website/college/units/1-2/making-a-camera/"}
---

## Process

![](https://lh4.googleusercontent.com/TfuxJdC2zTUEB1J6kb4JnpnPH7JeeNogjn_Z0bTBuOJnQqTEhf3WZgn61318VTppshK9uFpey-idCSHI1XOjK-I)

Import references for all angles, making sure to line them up in 3D space

![](https://lh5.googleusercontent.com/Xa3RGfRDKnG4UgQUpq2WMH367u3Sg_G75YCL5E_XkjRqPmh5AtxSnSx0bmGOC62Fz30HM6DmpzSMEdD5kAcZo0s)

Make some basic shapes and line them up with the references

![](https://lh4.googleusercontent.com/x2b6-oAh1_H88FhpfiCS_NosAFfF8k9G3K3Xn0sTyI88l6qu52X2F7Zp_s7Zoo-sG7gIZWh5zg75jiwncS5iJ2A)

![](https://lh5.googleusercontent.com/w5j2K_HWcloswbO-hlytpLiKEScpSvVvNpWCFp9aa9miHzUZ8Ub9id3a8hj8_joxjv_X8LMixYOa0XOGAIpxAQ)

Use more loopcuts to make a more detailed mesh

![](https://lh3.googleusercontent.com/a_wx7EKacXPhvHvKuiVm3rULImNgCQpgFESFW8-bff_1vni6P4FRl1N6mwwzM4eDaTO45z1A5PPnqVuNgpb4kqA)

With a little more tweaking we get a *fine* shape

![](https://lh3.googleusercontent.com/lwVr55mPFSyfeNVpv5r0xnj330s2ZQRibnFhoqlMkbMRRvQ5pWnR1SLsssAQNgcGKGyvxRYTuGk8iVSA6PSOc78)

Let's remesh it to create a sculptable mesh with an extreme poly count

![](https://lh3.googleusercontent.com/D1fiKyPE0JyQPdxEr9R43xwuaiQC1zu8K_ycA2-0-18p-zdzsHoA0qHc-QRvlzoajyeS7O2vMgh0r8D8VAPUpt4)

With alot of sculting and some bolean modifiers (like in the sensor location) we get a presentable body.

![](https://lh3.googleusercontent.com/wbVKtohH7xlXkjWsuYrZ77dxh1jHI-A_9rDnJEyY_glnc6YB9IxDLSe0BSZDq5qvPdscpAwzJlun_ko1KPV_D4w)

We can now add some little meshes for parts of the camera using multiple techniques. Most of the smaller things are just cylinders sticking out of the mesh, but larger things like the grips are 2d meshes shrink wrapped onto the body.

![](https://lh6.googleusercontent.com/Dd9PmD95QtWxR_VISbShyw2tvR9-80XTJKvtnDO5CW6msR36cCtnQ_38iQ-L5uRMu0q1mbwIyuuujPOTg6YezZ8)

The lens is made mostly of cylinders with inset faces extruded on individual normals.

![](https://lh6.googleusercontent.com/OrMMHPJ-typh5PFF67cSyZ9AlGKIwbSWNHNNqL5DY3OaxAPmqJM3X-NORstK1svS1kuAtgJs1mdae0MaNLE-jd8)

The inside of the lens contains all of the correct optics for a functioning camera, unfortunately I did not want to render through this as it would have taken 3hr+ for each frame and I would have had to render multiple times to focus it.

I added materials for all the parts...

![](https://lh6.googleusercontent.com/QXj5qr3ZwukIMltAvX9GhIbIHCDJ0dBCF5Nk9jxG6ruDeEbrxpOdH1lFVbBKuttzreTe_CUg2GpFmZ6DU8rpCYA)

And applied them

![](https://lh6.googleusercontent.com/alO5OXkdr3lmVU-hiUd82zWt78cO30lmAWq2YJDG2znesR63lXgVPBizSqdkEwIQq89LzkK4TyQftp8wo443z-I)

Lets set up a scene with a simple plane for the floor and two lights

![](https://lh3.googleusercontent.com/yKjrN9c_PLdKlp8q_-m2Awo7Uu7AuOjm7uAR1E8-OA1FLx7ZR0moqhlQ3qyN6ONauXBzmomR5EMCLHgh8tBEGiM)

![](https://lh5.googleusercontent.com/E3p619PZZlftO7FUsPv-N3pgZ2a7LI_RrI7QB7_wIF8WWWdGuqbCW6v2aIRq4dBoHBm6owrnjAoFyWOaWIYu_KI)

We can now make some keyframes for an animation of the camera, trying to keep movements smooth and satisfying. Before clicking render and waiting a few hours for the final result:

![](https://lh6.googleusercontent.com/dh497fByHam7wa-h6GT-Df2IQGN8Td1zcfaqDJctU0nlPI_vQznTG_O0KT7d0mw8lomeC2WhLDW9d43IwmeVkCs)

![](https://lh5.googleusercontent.com/kdQY7k3XlYHxNDatwVOKhRKxHbwTtnJ10u6zdJ2SRYUCZA_7Nc9h48M7N6HZ-W96ZaAPZXlV2bEB_h-CUTEaiF8)

## Evaluation

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

  
  

![](https://lh4.googleusercontent.com/qIpCHCka-c1fRR1xMfbaYr8W9VQJSn2vkn4Q9hDkO-D83C93bR642FnTS0lPVfyx4n3Tn5VkIITlHK4gNoT9qqQ)

# Framing