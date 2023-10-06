# Nextrevo mod
Using E3D Revo nozzles with Prusa Nextruder

# Disclaimer

This is not a guide.

This is a description of how I fitted an E3D Revo nozzle and heater to my Prusa Nextruder.
I do not claim that this is a good idea, or that this is the best way to do it if it was.
It's not even written as a guide. This is my story. It's long, because I like typing.

I take no responsibility for anything that happens to your printer, tools or person.

# Step 0 - Why?

First of all - Science isn't about why. It's about why not.

Second - I had just invested fully in the Revo ecosystem right before the MK4 was announced. Wah wah.
I didn't need the upgrade, obviosuly, but I wanted it because this is my hobby and I like tinkering with my printer.
Now the Revo investment won't be wasted money.

# Step 1 - Studies

As soon as photos of the nextruder started surfacing, I started thinking.

Didn't the whole idea look kind of familiar?
I took measurements on the pixelated photos, and an idea started to form.
I even bought a [Nextruder V6 Nozzle Adapter](https://www.prusa3d.com/product/nextruder-v6-nozzle-adapter/) long before I had a nextruder just to take more measurements.

When I finally got my MK3.9 upgrade kit, I was confident enough to just go for it...
Here's how I did it.

# Step 2 - Heatsink preparation

This was the part where the whole thing would stand and fall, but when I finally got a nextruder heatsinkin my hand, my hopes rose.

Excusing my limited CAD skills, this is roughly what the heatsink looks like:
![bild](https://github.com/thomasloven/nextrevo/assets/1299821/4a532d0e-44fc-4e78-b266-ca26ec9d3eb7)

And after probing around a bit, this is what the bore seems to look like on the inside.
![bild](https://github.com/thomasloven/nextrevo/assets/1299821/d23ca4dc-7494-4e5e-b35b-af361f61d12b)

I realized that the copper part of the Nextruder nozzle had the same outer diameter as the M4 threads of the Revo nozzle. It was also slightly shorter.

And guess what? The stainless steel tube of the Nextruder nozzle had very nearly the exact right diameter for an M4 threaded hole prebore.

So I went to work with an M4 thread tap. The goal was to deepen the hole with a thread like this:

![bild](https://github.com/thomasloven/nextrevo/assets/1299821/9184f35e-5adb-430b-bc50-86e3350e9f47)
![bild](https://github.com/thomasloven/nextrevo/assets/1299821/76971554-0be5-45ac-8802-b51b6584f7b1)

Very, very carefully, I cut threads until the Revo nozzle *just* bottomed out.

![IMG_6825](https://github.com/thomasloven/nextrevo/assets/1299821/0139a0b2-c6c0-4116-a2e4-2ec2e96694a7)

As best as I can tell, there are a little more than three full threads of contact, which I've heard is the minimal target rule of thumb for general mechanical design.

![bild](https://github.com/thomasloven/nextrevo/assets/1299821/c1f8fae8-a96e-4c39-9c8d-62bd3840f65f)

I then cleaned everything off carefully. Blowing out any shavings etc.

If you decide to try this, please don't do it with things already assembled.

For the next step, I assembled the Nextruder up until the [planetary gears were covered](https://help.prusa3d.com/guide/5-nextruder-assembly_434014#437006).

# Step 3 - Nozzle preparation

In order to guide the filament from the extruder gear and down to the Revo nozzle, I decided to cut off a piece of the V6 Nozzle Adapter I got earlier with a Dremel diamond cutting disk.

![bild](https://github.com/thomasloven/nextrevo/assets/1299821/53f598d0-3ecf-4ecd-98ce-fd29e380b98b)
![IMG_6832](https://github.com/thomasloven/nextrevo/assets/1299821/135f170d-51f5-47dc-9504-7ed06c2d7073)
Then I put the top part in the chuck of my drill chuck and spun it against a metal file to slowly get it to the right length.
I kept rechecking the combination of revo nozzle and steel tube in the partially assembled nextruder until I got a fit that seemed right.

I cooled the tube in water frequently, and made sure to chamfer the cut edge slightly and to clean it from metal shavings before each test fit.

The steel tube is not attached to the Revo nozzle. It's just held in place in the heatsink by the top thumbscrew, and stays in place when swapping nozzles.

# Step 4 - The Heater

Every single step of the way, I expected to run into the final roadblock that killed the entire idea. The next one was the Revo heater.

Turns out it's very similar to the Nextruder one. 24V 40W heater, 100 kOhm NTC thermistor...

The spring holding it to the original Revo heatsink comes off by just a firm pull, and the wire harness had to be carefully bent slightly with pliers such that it can fit below the heatsink and have the cables reach.

![IMG_6836](https://github.com/thomasloven/nextrevo/assets/1299821/2a566777-79b2-46ce-a11b-65352a07bf89)

> Note: The cables going to the heater and thermistor of the Revo heater core are held firmly by a metal bracket to provide strain relief. I really really like this. More on that soon.

The final, scarriest, part was how to connect the heater block to the Loveboard.

The heater itself was no problem. The cable had exactly the right length and right connector.




Ther thermistor was another story. Prusa uses a connector called Molex Clik-mate which seems to be rather new and hard to source.
After looking through various sites, it turned out that the cheapest way to get one was actually to have a whole new [thermistor](https://www.prusa3d.com/product/thermistor-ntc-100k-90-mm/) shipped from Prusa.

So I put in my order. It's expected to arrive next Tuesday.

"Luckily" - in **massive** quotes - I ran into other issues. Remember what I said about the strain relief of the wires on the Revo? Guess which heater doesn't have this?

After removing and remoutning the nozzle-heater combo as recommended **TWICE**, the cables to the heater cartridge of my only Nextruder heat block broke.

Prusa support is excellent as always, and a new cartridge is on its way, but this made me decide to just Leroy Jenkins it and cut off the connector from my only Prusa thermistor.

And now for the really scarry part. Did you know it's really really REALLY hard to solder heater block wires? Like impossible, because they are aluminium?

Turns out the thermistor wires are not, and can be soldered freely. The woven insulation can't easily be peeled, but it can be pushed back slightly and held in place with a bobby pin or something while soldering. It then closes up nicely.

![IMG_6838](https://github.com/thomasloven/nextrevo/assets/1299821/d7701a17-8451-45e3-8be5-070ca43bb086)

I put some electrical tape on it for safety too.

I took this opportunity to elongate the thermistor wire slightly, like 5-10 mm for a better fit.

And then it was done!

# Step 5 - Testing

Everything was done.

I routed and connected the wires, I screwed in a nozzle. I turned the printer on

I held my breath.

And it just worked!

Everything worked!

This far I have about 13 hours of print time on the Nextrevo, as I've come to call it, with mostly PLA but also a 2 hr print in PETG. I've make half a dozen nozzle swaps.

There is obviously much less contact area between the nozzle and heatsink than with a Nextruder nozzle, but so far I have seen nothing indicating e.g. heat creep.
I'll try to make some heat flow simulations and add them here at some point.

I've gotten no Thermal Model warnings - though I suspect that is because the thermal model is not actually implemented in the MK 3.9/4 firmware yet...

Input shaping seems not to be significantly affected.
Here it is printing the BonkersBenchy in 12 minutes:

https://github.com/thomasloven/nextrevo/assets/1299821/6d378369-aaa6-4bcf-801c-68ac932486da

This mod should be fully backwards compatible. I ran my first few test prints before the heater cartridge broke with the modified heatsink and stock Nextruder heater and nozzle.
