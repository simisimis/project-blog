# Inspiration / Motivation
It started years ago, pretty much the next day we moved into our new house in a scorching sunny land. As we were still settling in, I had to move some cacti out of our way. I thought sunny balcony is exactly what they needed. I was wrong. Withing the first day, half of the cacti were 'boiled'. The other half only partially damaged. Then I realized that the only thing that can go there is solar panels. But any bigger work that wasn't hanging paintings was moved to the backlog as we had plenty on our plate.
Same happened a year ago. We got an EV. I thought - finally I can utilize the 3 phase output. I went shopping and a couple of hours into my research I gave up. Charging stations were coming with their proprietary cloud apps, home-assistant integration was poor or non existant and charging with 8A over 220V using Schuko plug through Shelly smart plug was good enough. So I gave up searching and moved this task to the backlog. Until one day I tried removing that plug and I realized that this constant 8A power drawing over the single phase socket isn't as good of a solution as I thought. Shelly plug contacts 'fused' with a wall socket. Contacts welded and plastic parts around - melted. I started searching online and I saw that it was a mistake to use a Shelly plug for EV charging. I learned it the hard way.
So I restarted my research. My goal was simple. The car should start/stop charging only on particular hours. Daily. Only thing I should do - plug in the charging cable. To my surprise, what I thought should be in every EV car app or charging station settings - it wasn't. My car's app would only allow to offset charging by some hours(one time) 🤯
Smart plugs that could handle such loads also seem to not exist.
But as I was starting to get anxious(again) about the pricy wallbox chargers with their cloud applications I found one product - `Smart EVSE`. Looking further into it I was hooked! It was exactly what I was looking for and more! More on it later.
In the meantime, my partner during one of our morning standups mentioned that she saw plug-and-play solar panel solutions with integrated inverters that the only thing you need to do is - plug into your wall socket. And there it was, a beautiful entrance of a rabbit hole that I went head down.
In short - what was a task to replace a breaking Smart plug became 2 big projects: DIY charging station and balcony solar panel setup. 

# Shopping List

## Measurement

- Shelly 3EM Pro with 3x CT clamps(120eu)
- Shelly 3EM Pro with 1x CT clamps(120eu)

## Balcony solar panels

With a 400+ message thread on Slack eventually I settled on this:
- EcoFlow Stream Ultra with 4 PV inputs(total 2kW) and a 1.9kWh battery(~700eu).
- Locally available 465W solar panels. Mostly due to their dimensions. (3x90eu)

## EV charging
- Smart EVSE components (~320eu)
- Type-2 plug (~50eu)
- 5x 2.5mm2 wires (P1,P2,P3,N,PE)
- channels to hide the cables

# The Process / Pr(👹)ss
These were 2 different tasks, but it made sense to work on them simultaineously.
