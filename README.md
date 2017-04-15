# thingie

Thingie is a virtual embedded device that runs a very simple language and can be interacted with through an ascii art rendering of a screen, buttons, knobs, etc.

Users can submit their code and Thingie loads a new script every hour. Anyone using Thingie in that time will interact with Thingie running that script.

Thingie has it's own interpreter to run the code written in ThingieScript.

Thingie's peripherals:

- 16x2 character screen
- 4 pushbuttons
- 4 flip switches
- 2 stepped knobs (an 8 step one and a 4 step one)

Thingie also has 8 memory registers. 4 registers can store up to 16 ascii characters, the other 4 can store up to 16 integers between -9999 and 9999.
The screen's two lines are the 9th and 10th, special registers. 
Only characters can be written to them, otherwise they are written to the same way as other memory registers. 

## ThingieScript

ThingieScript is a simple language that can:

- read and write memory registers
- read current state of input peripherals
- perform basic arithmetic
- compare two values (both character and integer, result of comparison will be 1 or 0)
- control program flow with `goto`
- use "if" for conditional code execution
- wait for set length of time before continuing execution

Looping can be achieved with a combination of `if` and `goto`.
