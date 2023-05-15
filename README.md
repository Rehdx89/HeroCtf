
## Chosing class 
The first thing I had to do was to choose a class, there are multiple classes:
- Mage 
- Demon 
- Paladin
- Warrior 
- Ninja 
- Ogre
I took the Ogre bc he had 10 in strenght (which didn't even matter bc the enemies with lower strenght hit harder),10 in defense and 150hp. 

## What should I do now
In this part I had a message telling there is nothing to do and asking me what should I do, I looked into act() and saw the compare method being used which meant, I had some predefined inputs:


![[Capture d’écran (54).png]]

There are the things you have to say, I always said runnaway bc it was the most successful at breaking me out of the loop: 
![[Capture d’écran (55).png]]

## Where flag?
When killing enemies they sometimes drop things, but there's two setup_drop functions, setup_drop() and setup_drop_w, as we can see below, setup_drop_w() is only drops weapons:

![[Pasted image 20230515211419.png]]

But setup_drop() is way more interesting:

![[Pasted image 20230515211712.png]]

As you can see, there are two print flag functions, we need both, but to get to these print flag we compare something, it's the name of the enemies, it's looking for two enemies but idk what enemies so I had to debug it and see what was the enemies in question:

![[Capture d’écran (58).png]]
![[Capture d’écran (59).png]]

They're the two enemies to kill to have the flag, but they rarely appear, the flag was in two parts:
- Hero{YoureSomeKindOfDarkS
- oulsPlayerOrYouHighOnSmthWtf?}
flag : Hero{YoureSomeKindOfDarkSoulsPlayerOrYouHighOnSmthWtf?}