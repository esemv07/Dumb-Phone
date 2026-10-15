# Journal

This is the story of my process of making this project :)

### Total Time so Far: 1 hour 30 mins


## 15th October 2026
`Prototyping` `Documentation`

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

`Prototyping: +1 hour`

***+1 hour 30 mins***

### Time Spent on This Day: 1 hour 30 mins

`Prototyping 1 hour` `Documentation: 30 mins`
