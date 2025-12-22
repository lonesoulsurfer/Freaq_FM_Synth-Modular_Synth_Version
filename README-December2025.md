# Freaq FM Synth Instructables Update

I did not write the awesome original instructable but using that instructable built 4 of these Dec 2025 in the US:
![IMG_7258](https://github.com/user-attachments/assets/fbbd525d-b0ba-4a65-be67-d64e0d7035ba)

Here's a few tips and tricks I picked up along the way

## Circuit board and Front Panel

1. I ordered the PCB and front panel from [AllPCB](https://www.allpcb.com/). They did a great job but were unhappy with the front panel as they considered the gerber files incomplete.
They worked with me to complete them and we ended up with [this gerber file](Gerber%20Files/Freaq%20-Front%20Panel%20Gerber%20AllPCB%20Dec2025.zip) for the front panel.
1. The holes in the front panel for the pushbutton switches I sourced below were just a bit too small. I drilled them out with a 9/32" drill bit.

## Amazon Parts List

*I could not find many of the parts listed in the original instructable. Here's what I ended up ordering*

| Part  | Type | Value | Qty | Amazon Link |
| ------------- |-------------| -------------| -------------| -------------|
| Cap | Polypropylene | 104j | 100nf | 2 |https://www.amazon.com/dp/B0F1JRQVL8 |
| Cap | | 100uF | 2 |https://www.amazon.com/dp/B0D78PZQVL |
| Cap | | 1000uF | 1 |https://www.amazon.com/dp/B0D78Q46Z5 |
| Resistor |Metal Film | 10K | 1 |https://www.amazon.com/dp/B08QR76DHJ *these worked but better to get 1/4 watt instead*|
| Resistor | Metal Film | 270 | 1 |https://www.amazon.com/dp/B09B1NGH6Z |
| Potentiometer | | 10K | 8 |https://www.amazon.com/dp/B0DN1DHWLR |
| Knobs |For Potentiometers| | 8 | https://www.amazon.com/dp/B081P7G42P|
| Switch | Pushbutton | | 6 |https://www.amazon.com/dp/B07KX24622 |
| Switch | Toggle | | 1 |https://www.amazon.com/dp/B075RDYMQQ |
| LED | Dot Matrix 8x8 | | 1 |https://www.amazon.com/dp/B09Y399S84 |
| Header Pins | Female | 15 Pin | 2 |*didn't source* |
| Arduino Nano | | | 1 |https://www.amazon.com/dp/B086GNYXPH | |
| Audio Jack | 3.5mm female | | 3 |https://www.amazon.com/dp/B0CF9DQYQ6 | |
| JST Connector | mini w/ wire | | 1 | *didn't use* |

## Tips when assembling
1. As is, many of the parts listed above do not fit into the through-holes of the circuit board. Instead, they have "loops" at the end of their legs.
With small snips, cut the loops in half and bend so that half the loop will fit in the through-hole of the circuit board. See the below picture as an example with the pushbutton switch. Unmodified switch is on the left and modified on the right:
![IMG_7262](https://github.com/user-attachments/assets/a3654beb-7d15-49c6-b5ae-74aa58c95768)

1. Assemble all the components on the back side of the board first
1. Next, add the 8x8 LED
1. The remaining parts are various heights. To line them up on the front panel:
   1. place a subset of 1 or more parts on circuit board but do not solder yet
   1. attach front panel. Screw the part(s) into the panel so it is lined up and secure
   1. Finally solder the part(s) into place.
1. Following the above procedure, install the pushbutton switches. To reiterate as well as offer a specific example of the procedure:
   1. place 3 switches on one side of the board. Do not solder.
   1. attach front panel. Screw switches in place so they line up perfectly on the board.
   1. solder switches onto board with front panel still in place.
   1. remove panel
   1. repeat this procedure for the 3 switches on the other side.
1. Following the above procedure, install the toggle switch, then the audio jacks.
1. When soldering the audio jacks, with the front panel still secured and the jacks soldered in place,
flip the unit upside down and slip a piece of thin wire between the jack and circuit board to make a ground connection between the jack and board:
![IMG_7263](https://github.com/user-attachments/assets/e84fcee1-220e-4dac-bbde-0153e6d9114b)
1. Still following the above procedure, install the potentiometers.

## Case
[This case](https://www.thingiverse.com/thing:6944323) works great! M3 nuts fit into the channels perfectly. I bolted the rest together with M2 nuts and bolts because that's what I had but I would expect M2.5 or M3 to work as well.

## Final Thoughts
This synth is a blast to play with and I highly recommend it! And remember if you don't want to assemble it yourself you can always [buy an updated preassembled version](https://wireheadinstruments.com/freaq-fm) and support the inventor.
