# Bomber
A game for the Atari 2600 in 6502 Assembly

Hello, for my major project I made a game for the atari 2600 in 6502 Assembly. The links I sent you were a link to an emulator,  a cart.bin file which acts as the cartridge.

https://javatari.org/

Insert it into the emulator and you can play the game

On the game you can see a play field, scoreboard, missels, and two players on the screen at a time, sprites, and warp boarder to the left and right, and background sound. You may be thinking a number of questions which I will try to guess and answer


# What parts of the Major Project triangle did you hit?
I believe I hit the learn and time. I spent around 20 hours on this project taking notes, learning the 6502 language and coding and testing. I could've spent more time but I had some assembly knowledge going into this project that I could manipulate and mess around with. And learn, I made this game using Ubuntu linux and Vim which I have never used before, also I taught myself 6502 Assembly language. I also never coded a game with assembly before which is exactly how it sounds.

# But as a CE haven't you already taken an assembly class?
Yeah, actually I have, I took Assembly and Embedded Systems and I learned ARM Assembly and a little C and loaded them onto a circuit boards to play with. Unsurprisingly, 6502 Assembly and ARM Assembly are different, but similar in many ways. This was the first time I taught myself a different version of a language and successfully make a game. Some cool similarities I saw in the syntax were when you want to make a jump in ARM Assembly  you put:

Loop
    random code
    B Loop
    
When the code runs through the Loop and executes the code, when it hits the B it will immediatly loop back to what the following label is, which is 'Loop'. But for 6502

Loop:
     random code
     jmp Loop
     
The syntax difference is 6502 has the user type a : next to the label for the loop and jmp instead of B. This is of course extremely small difference but I found it interesting.
Also, for my class I was mainly working with arithmetic problems and manipulating roughly 7-14 registers. Whereas coding for the atari the registers are mainly named based on the code. ldx is loading a value into X. In the code below, we are loading the value #$80 into X and then storing that X value into the memory COLUBK which controls the background color on the atari.
     ldx #$80     ; blue background color
     stx COLUBK
     lda #$1C     ; yellow playfield color
     sta COLUPF
Something that I actually despise about 6502 coding is how we label numbers. Understanding binary and hexadecimal arithmetic is extremely essential for coding in assembly. In ARM Assembly it doesn't matter what form the number is as long as it is after a #. in 6502 if the number is a decimal it is just #, if it is hexadecimal it has a $ in front of the number not a 0x, and if it is a binary it has a % in front of the number not a 2_. Makes me boil and took a bit to get used to.

# What was the hardest thing about the project?
Honestly, the way beginning when I was deciding what code editor to use and also trying to incorporate linux with it. I was using atom on windows and all the wrong terminals. Git bash wasn't working and my emulator (I personally used Stella which is different from the one I sent you because it is better to use when debugging). So I gave up and booted up Ubuntu and Vim. This was my first time using linux for honestly anything so dummy me had 400 tabs open for trying to figure out how to exit a VIM file. It was also my first time using vim, which was ok, there are probably easier way to navigate and utilize vim to its max potential but I used it and figured out what works best for me. As a CE, I know linux is a very important tool to know in the workforce when working with low level languages. So I'm happy I learned a bit of linux and getting comfortable (and very very angry) in a terminal.

