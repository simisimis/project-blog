# Motivation

- We have an all year round sunny roof balcony
- There exist plug-and-play balcony solar solutions
- Everyhing in our house is running on electricity. Even a car.
- Surplus energy should be stored in a battery rather than exported to the grid.

Simple math really, when you put these points together there's only one way forward...

# Components

- EkoFlow STREAM Ultra 4pv 500W inputs with 1.92kWh battery
- 3x 465W Solar panels
- 2x Shelly 3EM Pro
- Wood for the frame

# Installation notes

## Physical installation

At the time of writing solar energy is not regulated. Because I did not want anyone knocking at my door I wanted Zero feed-in setup.
Another constraint: In Greece even if I own the apartment, I do not own the outside walls. Because I did not want to spend my time figuring out what is allowed and what is not I wanted a setup that would not require drilling or in any way messing up with the apartments walls or balcony floor. 
I decided to build a wooden frame and mount the panels on it. EkoFlow STREAM ultra is rain/dust resistant so it went nicely under one of the panels. Set up was done.

## Electric wiring

Electricity part was a little more complex. I reached out in a local community with my questions, I received loads of information. Long story short, for EcoFlow to know how much solar power it can push into the network, it needs to know the load of the phase it's connected to. I tried finding an electrician to install Shelly 3EM Pro in my electricity closet however while waiting for the response I started looking into my closet and saw that it's not that difficult of a task, so I decided to do it on my own.
Figuring out wiring wasn't obvious because it's a 2 floor apartment with a garage. But eventually I did the following:
- Figured out the phases and mapped what appliances were connected where.
- I saw that EkoFlow was connecting to a socket on phase 1. So I changed the circuit feeding my 3d printer/server closet/and my office room devices to be on the same phace as the solar panels
- Made sure 1 phase EV charging was also using the same phase

## Configuration

For EkoFlow to know how much electricity it can push to the household it needs to know the load of that one phase. So I installed Shelly that only has CT clamped on phase 1. But after I saw how useful was to see the precice load on all 3 phases, I bought and installed another one to be able to monitor my house consumption.

Setting up the Shellies was an easy task. As for EkoFlow, initial set up was super easy, however to fine tune it, I had to fiddle a little until I learned what meant what. Took me a couple of days until I was happy with how it was set up.


# Lessons learned

The biggest disappointment in this project was learning how partial shade affect the charging rates. Somehow I didn't know that until was in the last phases of setting things up. Even 10-15% shade diagonally/vertically or horizontally would drop charging rates from 365W to 120-180W. This is especially big loss in a balcony that has less than 2h of full sun. I am confident my 3 panels are delivering 1/3 or 1/4 of it's max potential. During the summer months I am getting 3-4kWh per day. We will see how that will change now that the winter is coming.
Also I had one accident, when a summer storm lifted one panel off the floor like it was a piece of paper. I was very lucky as it ended without casualties. I did not test my luck twice.

# Conclusion

I learned a lot in the process. Luckily I had no major step backs and the whole process went mostly as I hoped it to go.
