# The Process/Pr(👹)ss

## Things to do so I would not do... Things

- Learn Blender so I could design the cases.
- Learn KiCAD so I could design needed PCB.
- Learn things like I2C, USB HID
- Learn programming embedded
- Probably need to also learn debugging..
- Nixos has to support needed tooling
- To be continued...

## The beginning

It was like a big bang. It started with a tiny spark and instant chain reaction got me in a chaos of parallel sub big bangs. If that makes sense... 😅
One thing was clear - I wanted to make a keyboard that I could attempt to run with Rust based firmware.
I kept finding myself spending hours trying to solve emerging obstables, but then they would branch out to the point that I would need to step back and start from the beginning.
I'm only going to mention a couple of them, but there were many and on every corner.

### Handwire or go PCB way

It was so tempting to just grab a carton, stick some switches in it and start figuring out how to program a controller.
And I did, picked a keyboard shape that made sense to me and 3d printed an outline where I could stick those switches. After spending 6+ years with ergonomic keyboards(2+ years with split) I knew I wanted it to be as small and column staggered, but I wanted it to be monoblock. So when I saw Absolem and an article about it, it solved all the things I was trying to solve. I don't have much experience making PCBs apart from a project from 25 years ago when I made a stroboscope that included painting with nail polish traces and etching the rest of the copper with an acid. Handwiring was very appealing, since designing a pcb felt overcomplicated and daunting. But handwiring meant higher profile as well Cherry MX, while I wanted hot swappable Kailh Chocs. And there I was split between two paths. Learning about both processes and changing my opinion which way to go pretty much every two hours.. For over a week. In the meantime I was trying to solve all other problems like...

### Picking an MCU

What a journey here. Initial requirements were - Rust firmware support. I did not even know if this project would be more about making a keyboard or a way to learn Rust in embedded.

After a week I just thought I will order a couple of all controllers that were considered and make this decision later as I will actually start doing something and stop planning.
With Current Esspresif PRO-Rust mindset I wanted to go with ESP32 RISC-V based MCUs, I already had ESP32-C6 devkits that I could just pick and use. Apparently not, I learned from specs they couldn't be programmed as HID devices.

Quickly it became a battle between Promicro, nice!nano, nfr52, stm32, rp2040 based devices. I couldn't make up my mind yet again. Go wired or Bluetooth. Some supported by QMK, some by ZMK, some limited by licenses, some too old to base my future on. At this point I had already given up the idea to program it in Rust. Eventually found a GH user who got Keyberon firmware on nice!nano. That gave me confidence, at least for now, so I started shopping for...

### Keyboard features

Since all of these considerations were happening in parallel, a list of features kept increasing and decreasing every couple of hours. Switches, LEDs, rotary encoders, BLE HID, trackpad, trackball, OLED screens, battery.

____

I knew that this was a big bite and I knew that to successfully swallow it, I need to chew it really well. All I had to do is put time and effort at a steady pace and eventually things will stop branching out and instead will start falling into places.
