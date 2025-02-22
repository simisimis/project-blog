### Just put time and effort...
Famous last words... Of mine...
It appears putting time and effort only continuously kept uncovering more things that I don't know. To the point that one evening I picked up Zelda TotK and disappeared for 7 months. I could not go back to the tangled mess that has been waiting for me where I left it. And with every day it was harder and harder to come back to it.

The break happened because a couple of things. A night before, I was up till 3 a.m. I spent perfecting trace paths and connecting the nets. I wanted to finish because next morning we were supposed to go for a 2 week vacation and this was like a milestone I wanted to complete. That was a bad idea. Milestone gives a tiny sense of completion. That and a little break was a perfect coctail to not want to come back to where I left.

### Stockholm syndrome
It was forsaken, but not forgotten. Eventually psychological bond established with my captor came through and I picked it up again. While people were busy working on AoC, I went back to where I left. It took me a few days to remember where was I and what I was doing before I stopped. i.e. just ergogen config was already 800+ LoC that I did not know how to navigate anymore. But I did get there. This time calmer and with confidence. And this is exactly why I love declarative approach. I was able to just jump into the nix dev shell and continue editing/adding.

### Electronics 101
I had the main parts wired, i.e. Keys, diodes, rows, colums, LEDs. Now I wanted to add remaining parts before I will move to ordering. It appeared that I had no idea about even most basic parts of electronics. I spent many hours watching YT about traces and its return path. To the point where I realized - all that pristine trace wiring work that I've done should go through the window and I need to rework it from scratch. This time however instead of slowly steering a horse with a carriage, I was was on a racing bike. Just in couple of days wiring has been completed.

### Electronics not so 101
To add the screen and the trackpad I had to start diving into datasheets. These pdfs surely know how to explode in your face. Not sure why, maybe because of tens of different voltages while I would expect one, or that all the info was in Mandarin... By then I already picked nice!nano mcu but now there were more things to consider. Can one controller drive all this. After I had all pins assigned to components I had zero pins left. Questions like - can a low speed digital pin drive data pin for 36 addressable LEDs? Do I have to add all this fluff for components like capacitors to stabilize power? Would it still work if I didn't? For how long? Will these LEDs light up with 3.3V even if datasheet is telling to use 5V, but controller doesn't output that. And the questions were all over the place. If I would check keyboard forums, they would skip many of recommended parts, while in electronics forums they would do it by the book.

This time however I just kept rolling. I had no deadline, no milestone to fulfill. Just one day at a time get one step closer to the end.

### Follow one's footprints
Just like in life, you can only go so far following someone's footprints. Very quicly I realized that if I want to keep using ergogen, I will have to be creating footprints myself. Thousands of products they all come so similar and so slightly different. That was such a daunting job I hoped to avoid, but was happy to learn that apart from tedious copy pasting work it wasn't nearly as bad as I have feared. I should mention however that at this point I have spent many hours in KiCAD and I started getting more and more familiar with it. Some I downloaded and templated some I had to create myself.


### One Goose’s Delight, Another’s Disgust
In the begining I was all about creating something that could be picked up and used by anyone who'd be interested in it. However organizing everything with that in mind soon made little to no sense. This is such a niche product and there are so many keyboards that were popularized and already widely adopted and nowadays you just order a kit, solder it and upload the kit and there you have it. Therefore I decided that if some one person will be interested in it, I would rather walk them through rather than create a fully consumable product that no one will ever even see.

### The leap of faith
And there it was. The keyboard that has been on my head for so long. Now it was feature complete. I was ready to place an order and get it manufactured. But there was tingling feeling that maybe something is still wrong and I will realize it right after I will send my order. And I checked. Tens of times. And every time I would find more things to fix. This made it really hard to just close my eyes and go for it. Eventually it happened. But I am happy I took the time to do it.

### Then there was silence
The waiting began. Now that project had a pause, I had time to start preparing myself for the next steps. The firmware. I thought I would need to fork repos and rewrite the software and deal with all the hell that will pour on me. Lucky for me, this was not the case. It does take time to get familiar with these things. But after all previous work this was a pleasant walk in the park. Still is. I'm not done.

### Due delivery day
Not much to comment here... Only maybe THAT IT WAS THE BEST THING EVER! That smile on your face when you unpack the pcbs and just look at them. How shiny, how perfect, how real they are... Boards haven't even had a single part on them and it already felt like my job there is done...

### Soldering
I grab a stencil, mount the board, start spreading the paste and... The paste is tough. It doesn't stick to the stencil or on pcb. Dragging it on one end, pulls from another. Starting to realize that all these YT videos advertising amazing led-less solder pastes and reflow heat plates is a LIE! Well it isn't if you know what you're doing. But After a couple of days me trying to solder everything with the paste and heat plate and cleaning it all with isopropyl alcohol and perfecting it over a digital microscope just to realize that keys work only if you twist the keyboard slightly... Constant reheating and resoldering most likely created tiny cracks or leftover solder paste was shorting something but I decided that it's time to take the second board. Along the way I also learned how tiny is the 0805 and how shaky my hands are. This soldering saga continued for a week or two.

### Rolling to production
After finally all rows and columns started working. After all keys started responding. After layout was created and configured. After LEDs started giving a nice xmassy feeling... It was time. Time to put the keyboard to a test. To monkey the type out of it. At this point I was already happy. I started thinking how I should just put a full stop on making it and start enjoying it. It worked! And as much as I was afraid staggering these colums so drastically, in the end it only took me 30 minutes to get back to my typing speed. My new split but not split keyboard...
I should end here.

### The end is never the end is never the...
And here we are today. Case is still not designed. Encoders glithing and triggering without being touched. Cirque that community is still in the process of taming. OLED screen that is most likely not going to work until a few lambs will not be sacrificed for the Gods. And me in front of it all already thinking about DeeDee v2. Or at the very least DeeDee v1.2...
