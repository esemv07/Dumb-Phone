---
title: "Dumb Phone"
github: "https://github.com/esemv07/Dumb-Phone"
description: "An all in one dumb phone device to remove distractions"
created_at: "2026-10-15"
total_time: "3h"
---

# Journal

This is the story of my process of making this project :)

***Total Time so Far: 3 hours***



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
## 17th October 2026: Finding a Display
`Research`

I found [this](https://www.aliexpress.com/item/1005008749154854.html) display which doesn't seem the need a driver as long as I pick an STM32 with integrated MIPI DSI hardware. I can add that to the list of parameters to narrow down which STM32 I can get. So far I think that this display is a good option, and unless something better comes up or I find a reason not to use it, I'll go with it.

<img width="220" height="220" alt="image" src="https://github.com/user-attachments/assets/963447d0-8689-4075-9827-052ecf4ae3af" />

Next I am going to look at a camera module which will work with an STM32 and also a speaker. I think I will end up going for bluetooth for the keyboard but I am still yet to do more research on whether this will work without the need for reconnection upon startup.

`Research: +30 mins`

***+30 mins***

#### Time Spent on This Day: 30 mins

`Research: 30 mins`

<br><br>
