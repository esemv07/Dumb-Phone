---
title: "Dumb Phone"
github: "https://github.com/esemv07/Dumb-Phone"
description: "An all in one dumb phone device to remove distractions"
created_at: "2026-10-15"
total_time: "9.5h"
---

# Journal

This is the story of my process of making this project :)

***Total Time so Far: 9 hours 30 mins***



## 15th October 2026: Finding Inspiration
`Prototyping` `Documentation` `Research`

This is the beginning of my journal! I am going to start by setting out the goals and intentions of this project, and just a brain-dump of my thoughts so far.

This is my first project which will not use a premade SBC like the Raspberry Pi as I want to make a custom PCB with the chip integrated.

This will help a lot with space conservation as I can place everything exactly where I want and will also just be a cool challenge because I have never done this before.

#### The Chip
I think I am going to use an STM32 chip but I'm not 100% sure which yet. I will try to write out all the components I need in order to try calculate the exact variation of the chip I will need.

I have never done this calculation process before so it is completely new to me. I'm pretty excited to try it and I hope I get it right as I really want this to work.

#### The Device
I want the device to be capable of:
- Vertical phone mode and horizontal palmtop mode
- Playing music from internet sources
- Notetaking in horizontal (and maybe vertical too) mode
- Foldout gamepad for gaming mode
- Camera on the back side

`Documentation: +30 mins`

I think in order to do this I will have to make my own firmware as it's unlikely there is something exactly like this out there. I want the switch from horizontal to vertical mode to be automatic based on the screen position. I am not 100% sure how I am going to do this yet but it will likely be something to do with it clicking into the vertical position vs. the horizontal position.

#### Initial Designs
I was inspired by this design from Pinterest:

<img width="736" height="594" alt="image" src="https://github.com/user-attachments/assets/c1709d3c-2ed5-4325-abc6-e3eded51b140" />


That's similar to how I want the screen mode change to work and then on top of that I want the keyboard to fold out to reveal a gamepad underneath. I am currently undecided whether I will thread a cord from the keyboard PCB to the screen or I will use Bluetooth. Bluetooth honestly seems more favourable but I haven't worked with it too much before so I'm not sure whether I would have to reconnect the keyboard every time the device is turned on (which would be annoying) or whether I can have it automatically connect. If it would auto connect I think I'll definitely go for Bluetooth as it would avoid annoying wiring issues.

I made a really simple cardboard mockup to visualise the idea. I think I'll end up making another more detailed one to help with prototyping and CAD and just visualise how all the parts fit together. I will add a photo of this design later.

<img width="400" height="225" alt="IMG_4900" src="https://github.com/user-attachments/assets/f8de4968-5882-4ad9-bd4f-8a4e7634bb7b" />

`Prototyping: +1 hour`

***+1 hour 30 mins***

I'm doing some research for inspiration for what I want the overall design to look like and the case so I'll dump the images here:

<img width="300" height="450" alt="image" src="https://github.com/user-attachments/assets/483cc05f-21bd-46c2-9249-efc6b8c04250" />

I really like the chamfered edges and angles on this design.


<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/1a1f5b09-574f-4d9d-bc52-ead2620caa5b" />

[This](https://www.reddit.com/r/blender/comments/142gwii/cyberdeck/) is particularly awesome and something I would like to emulate. The shaping is super nice and the side handles are a great touch. I'm not exactly sure how the sliding mechanism works in reality as it looks to only work as an animation so this is something I would have to consider.

<img width="537" height="400" alt="image" src="https://github.com/user-attachments/assets/2c836b20-68dd-478c-9dfd-480d4da84617" />

I just love this vibe, not that it practically looks anything like what mine would with all the features, but the vibe is awesome.

<img width="427" height="284" alt="image" src="https://github.com/user-attachments/assets/04b92a74-7b7c-4a27-b380-4469baefaf5c" />

This design is super cool and I'll have to have a look at how the sliding mechanism works. I've watched the [video](https://www.youtube.com/watch?v=gIWp_F9PPzI) before but I want to take a closer look this time so I can understand the mechanism. I notice I like a lot of the designs with chamfers rather than fillets so that's definitely something I'll have to go for.

<img width="540" height="304" alt="image" src="https://github.com/user-attachments/assets/a71da49f-69a7-4461-aa81-2147d4aaf6a0" />

I really like the handles on this design, I might add handles to mine, maybe for practicality maybe for aesthetics. The speakers are also quite an interesting touch

<img width="319" height="240" alt="image" src="https://github.com/user-attachments/assets/e7632d73-60cd-412d-b4d2-846701c0bc9e" />

This is a pretty interesting design too although I'm not sure whether it would have stability issues.

<img width="236" height="348" alt="image" src="https://github.com/user-attachments/assets/8c6bc6b4-5925-42a8-88af-0c9994d23cc4" />

I really like the shape of this which I'm sure is also comfortable to hold.

`Research: +30 mins`

***+30 mins***

#### Time Spent on This Day: 2 hours

`Prototyping 1 hour` `Documentation: 30 mins` `Research: 30 mins`

<br><br>
## 16th October 2026: A Little Research
`Research`

I was looking at some displays this morning and am trying to figure out how I can best conserve size. I would prefer a display that doesn't require a controller/driver board which I think means I have to go with SPI (not 100% sure if this is correct, I'm still doing more research).

I found [this](https://www.youtube.com/watch?v=7FxN6tjMZeU) video which I am going to refer to along the process to figure out which STM32 to go with. I first need to figure out any of the basic components such as display, speakers, camera module, etc. so I can figure out the specs I need.

`Research: +30 mins`

***+30 mins***

#### Time Spent on This Day: 30 mins

`Research: 30 mins`

<br><br>
## 17th October 2026: Finding a Display, Camera and Beginning the CAD
`Research` `CAD`

I found [this](https://www.aliexpress.com/item/1005008749154854.html) display which doesn't seem the need a driver as long as I pick an STM32 with integrated MIPI DSI hardware. I can add that to the list of parameters to narrow down which STM32 I can get. So far I think that this display is a good option, and unless something better comes up or I find a reason not to use it, I'll go with it.

<img width="220" height="220" alt="image" src="https://github.com/user-attachments/assets/963447d0-8689-4075-9827-052ecf4ae3af" />

Next I am going to look at a camera module which will work with an STM32 and also a speaker. I think I will end up going for bluetooth for the keyboard but I am still yet to do more research on whether this will work without the need for reconnection upon startup.

`Research: +15 mins`

***+15 mins***

Ok so I'm looking at cameras and immediately [this](https://www.aliexpress.com/item/1005007480635043.html) one caught my eye. I literally haven't looked at any others yet so I don't know whether I'll go with it yet. But there's a lot of different versions and I don't understand cameras so I'm going to have to research what the different versions mean and which to go with for my project.

<img width="220" height="220" alt="image" src="https://github.com/user-attachments/assets/8e178a62-b7cc-448b-b514-52170124b38d" />

`Research: +15 mins`

***+15 mins***

After a bit of research I have found out the iPhone 0.5 camera has 120 degrees of FOV. Unfortunately the 120 degree one isn't available but the 130 degree one is so I think I'll go with that one unless the 120 degree one comes back in stock before I am up to buying.

For the keyboard I want it to be quite small so instead of regular keyboard switches I will use soft tactile switches that will not be clicky and build my own keyboard with that. [These](https://www.aliexpress.com/item/1005012357933716.html) are pretty much what I'm looking for so I'll keep these in mind.

<img width="220" height="220" alt="image" src="https://github.com/user-attachments/assets/91935f23-b9fa-48d9-9c23-0777fb0ef705" />

I'm going to give modelling the case a try just for a first draft so I can see how everything would fit together. I am using OnShape as Fusion decided not to work anymore on my laptop :)

`Research: +15 mins`

***+15 mins***

I've made a basic shape for the base layer of the case as well as the bottom layer of the keyboard layer. I'm pretty happy with how the geometric chamfer shapes are looking and I also added a hinge to the bottom keyboard part.


<img width="426" height="250" alt="Screenshot 2026-10-17 at 7 16 16 pm" src="https://github.com/user-attachments/assets/d2a5fd40-6cb5-46f1-9247-b11fc7d00b02" />

<img width="477" height="230" alt="Screenshot 2026-10-17 at 7 17 05 pm" src="https://github.com/user-attachments/assets/471cc27c-19d8-4c57-93e8-26bd43606c24" />

`CAD: +45 mins`

***+45 mins***

I've found some more parts: a [segment display](https://www.aliexpress.com/item/1005006855177010.html) for displaying battery levels, a [joystick](https://www.aliexpress.com/item/1005006760485880.html) for the game controller, and some [tactile buttons](https://www.aliexpress.com/item/32815969627.html) for the game controller and the music player buttons.

<img width="220" height="220" alt="image" src="https://github.com/user-attachments/assets/7cb73573-18a3-4cf3-8154-2e7cfeb3d087" />

I think this is all the main parts (although I might be forgetting something) excluding any battery and power system. Next I will calculate what battery I will need and how I will handle power, I think I want USB-C charging. I will then hopefully be able to figure out exactly which STM32 I need and begin making the PCB with all this information.

`Research: +30 mins`

***+30 mins***

#### Time Spent on This Day: 2 hours

`Research: 1 hour 15 mins` `CAD: 45 mins`

<br><br>
## 19th October 2026: Finding Speakers and Continuing CAD
`Research` `CAD`

I was right, I did forget something: speakers. I have found a [headphone jack](https://www.aliexpress.com/item/1005005562777837.html) module and some [small speakers](https://www.aliexpress.com/item/1005006334311884.html) that should work perfectly with this.

`Research: +15 mins`

***+15 mins***

I refactored the hinges on my case and I think I like them a lot better now!

<img width="402" height="209" alt="Screenshot 2026-10-20 at 6 51 49 am" src="https://github.com/user-attachments/assets/5defee77-9e9c-48d6-be7e-0ee67f930728" />
<br>
<img width="460" height="318" alt="Screenshot 2026-10-20 at 6 52 21 am" src="https://github.com/user-attachments/assets/0d7fd4d4-6287-453c-a29c-8c8e358f9c2d" />
<img width="448" height="240" alt="Screenshot 2026-10-20 at 6 52 50 am" src="https://github.com/user-attachments/assets/1701311a-6b12-4a68-b6b7-90f034865da2" />

`CAD: +45 mins`

***+45 mins***

#### Time Spent on This Day: 1 hour

`Research: 15 mins` `CAD: 45 mins`
<br><br>
## 20th October 2026: Researching Screen Connections
`Research` `CAD`

Ok so I think it is going to be too hard to have a screen without a driver that also connects by Bluetooth to the keyboard and STM32. Instead I am going to make the enclosure around fitting the driver board while still making sure to conserve space as best as possible.

I was thinking that having the screen connect by cable would be annoying as it would hinder the sliding mechanism but then I remembered [this](https://www.techeblog.com/jankbu-sliding-screen-modular-cyberdeck/) Cyberdeck that I previously saw. It uses a CNC type cable holder so that the screen can slide. I think I will try to emulate this but on the edge side of the screen so that it can also tilt upwards once it reaches the end of the slide.

<img width="360" height="225" alt="Screenshot 2026-10-20 at 7 48 15 am" src="https://github.com/user-attachments/assets/cfbd7863-2cb8-41b6-836d-0450421ddaf6" />

This greatly widens my options for what screen to go with so I think I'll change what screen I'm going with for something easier and more well documented. It also reduces the parameters for my STM32 (I think) as I don't think I'll need MIPI capabilities anymore.

`Research: +45 mins`

***+45 mins***

I've made some updates to the hinges in my CAD model and I really like the way they're looking now. I also added a bottom panel to hold the PCB that will be at the bottom. I plan to put the main brains there and then have the other parts connected by ribbon cables as peripherals.

<img width="484" height="326" alt="Screenshot 2026-10-20 at 6 17 45 pm" src="https://github.com/user-attachments/assets/64c11707-c5f4-4ac8-b618-81c0ff308115" />
<img width="516" height="309" alt="Screenshot 2026-10-20 at 6 18 03 pm" src="https://github.com/user-attachments/assets/cb69dc09-7912-4fd0-9ebb-81890f2f998f" />

Next I will try to add the gap for the CNC sliding mechanism and see how I can model the sliding mechanism too.

`CAD: +45 mins`

***+45 mins***

#### Time Spent on This Day: 1 hour 30 mins

`Research: 45 mins` `CAD: 45 mins`
<br><br>
## 22nd October 2026: Making Cable Chains
`CAD` `Research`

I have made some cable chains similar to the CNC ones I researched and I think they will work great.

<img width="315" height="266" alt="Screenshot 2026-10-22 at 8 20 26 am" src="https://github.com/user-attachments/assets/f1f22449-3061-4404-a66d-c179ce6b511b" />

<img width="466" height="289" alt="Screenshot 2026-10-22 at 8 19 53 am" src="https://github.com/user-attachments/assets/8228f21f-9101-4eb0-84de-6aea43e8ed5b" />

I added some clearance that will hopefully be just enough that they slot together and stay together without needing any screws to slot in together.

Next I am going to try to model the rails for the screen slide so that the screen can move and be connected to the cable chain.

`CAD: +1 hour`

***+1 hour***

I've added the keyboard enclosure. I used the blackberry keyboard as a reference for the dimensions of the holes for the plate. I then also tried to add the sliding gap but I only added it on one side so far. I want to put a slot at the end so that when it is open then the screen can be held at a 'laptop-type' angle.

<img width="402" height="269" alt="Screenshot 2026-10-22 at 11 55 43 am" src="https://github.com/user-attachments/assets/cfe6cf03-5a4f-4023-a361-de6caa8abad5" />
<img width="815" height="657" alt="Screenshot 2026-10-22 at 11 57 12 am" src="https://github.com/user-attachments/assets/fbddd35e-7e04-4ecb-9b3b-8e16e1f993f4" />

I think [this](https://www.aliexpress.com/item/1005012748404459.html) will be an ok screen to go with, or at least it's the type I think I'll go for.

I think the ribbon cable will be too wide to fit in the cable chain and all the displays I could find had a similar width. So instead I will put the driver in the top of the case and then have the HDMI cable that goes in the cable chain.

`CAD: +1 hour` `Research: +30 mins`

***+1 hour 30 mins***

#### Time Spent on This Day: 2 hours 30 mins

`CAD: 2 hour` `Research: 30 mins`
<br><br>
