# Motivation

It's quite a simple list.
- Open source solution. I shouldn't need a yearly subscription or a 3rd party cloud service collecting my data to be able to schedule a car charge.
- When buying an appartment I had to walk an extra mile to get a 3 phase cable in our garage. Would be a waste not to use it.
- Native Home Assistant integration
- DIY!
- Price: ~3x cheaper.

# Components
Following Smart EVSE diagram I ordered the following parts:
- DC Residual Current Sensor
- Iskra Contactor 32A 4pole 230V
- Iskra Contactor 32A 2pole 230V
- Smart EVSE v3.1 controller - Network connections : WiFi
- Enclosure IP65 with DIN rail
They didn't have a connector on their store, so I bought one from AliExpress for 65eu
- Type-2 Female Socket 32A

With cables and housing total price was <400eu.

# Garage work

## Cable management

I had to make a decision, to put a charging station over the 3phase output. But then I would need a 12m cable. That is both expensive and not practical as we would be tripping over that cable all the time. Instead I chose to extend the cable in the channels along the wall. Nothing complex mostly just physical meticulous work getting these thick cables to go round the corners.

## Smart EVSE assembly

This was a very pleasant task. Diagram very simple. Just wire everything as in the picture. Mounted all the parts in the enclosure. Only thing that required a bit of careful handcrafting was cutting a hole in the enclosure to fit in the Type-2 socket.
I skipped some parts like locking mechanism or their sensorbox. At that time I thought I will be able to configure Smart EVSE to use data from my Shelly 3EM Pro. But later I learned it was not feasible. It's not a big deal for me as the panels do not produce enough power that I could use the charging station in solar mode.

## Setup notes

- I connected both 4pole and 2pole contactors. To be able to switch between 1 phase and 3 phase charging.
- Connecting it to Home Assistant was also very simple:
  - On Smart EVSE I configured my MQTT server.
  - On Home Assistant I created a script:
    - Set the current override to 8A
    - Turn on 3 phase mode
    - Put Smart EVSE into `Normal` mode.
  - On Home Assistant I created an automation:
    - daily at 2:00am and at 11am trigger the script
    - at 4am and at 3pm put Smart EVSE into `Off` mode.

That was it. Every day the charging station is charging 3x8A 2am - 4am and 11am - 3pm. And the only thing I need to do is to not forget to plug the car. If electricity provider will change the cheap hour window I will adjust that. If I will decide to charge it on one phase or on less current - will adjust.

## Lessons learned

I am happy that for once I had a project where I did not say - if I would do it again, I would do something differently.
