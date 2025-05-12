# HowardSt
Public repo for residents of 1233 Howard St

## WiFi

Several people asked me what I meant by ‘competition’ for WiFi traffic. I’ve tried to write up a short explainer, and some suggestions as to what we can do.

### Background 

Unlike a wired connection, where the only traffic on a wire is what’s transmitted by the two ends, radio waves are shared – radio signals spread in all directions and anything within range can her them. That means if two stations transmit at once, they interfere with each, and neither signal gets through. So how is WiFi designed to work with this restriction? 

An analogy might be a room with many people in it all trying to have conversations. In general, there are three techniques to help:
1. Don’t talk all at once; take turns (_timing_).
2. Talk only as loudly as needed for the person you are speaking to, to hear (_power_).
3. Talk at higher or lower pitches, as we can distinguish men’s and women’s voices even when they talk at once (_frequency_).

WiFi uses all three techniques. 

* _Power_: The ‘announcement’ packets (that enable your devices to tell you what WiFi systems it hears nearby) are sent at full power (but infrequently). Data traffic is automatically adjusted to be ‘just powerful enough’ to get through to the intended recipient.

* _Frequency_: There are a number of frequency bands (I think 18 or so) assigned for WiFi, and generally stations on different bands can transmit simultaneously without interfering with each other. In addition, after WiFi was first introduced on the 2.4GHz bands (some of which were shared with other uses), a large set of frequencies in the 5 GHz range was licensed for only WiFi usage.

* _Timing_: each transmitter (device and base station) listens on its chosen frequency until there seems to be no-one transmitting, and then tries to transmit. It’s nonetheless possible that two devices choose to transit at once, so they listen while transmitting and if they detect such a collision, they both stop, wait a random length of time (so they don’t both try to transmit at the same time again) and try again.

And, just as in our example of conversation, there is always the possibility of other noise – e.g. a jackhammer outside the room. In the WiFi case that can be faulty equipment (e.g. a microwave oven that leaks radio waves) or other non-wifi uses of the same frequency bands (some bands are shared).

If there are more systems, WiFi networks, than the number of frequency bands, the bands all get busy. And as more and more systems try to transmit on the same frequency, the time that each transmitter has to wait before it detects the frequency is free, gets longer; and each time that there is a collision, the random time that the station waits until trying again also gets longer. The result is that everyone using that frequency gets to share it roughly equally – and the number of packets they can transmit per second goes down, and hence the throughput each one experiences goes down. This is, I think, what we are experiencing – the radio waves get busy and everyone gets a smaller share of the throughput possible on each frequency.

### What can we do? 

* _Frequency setting_: The power control and timing are automatic in base stations. However, it’s possible to configure a base station to use a specific frequency. This is rarely a good idea: it’s generally better to let the base stations choose automatically. It may be worth checking your settings.

* _Modern equipment_: Make sure you have modern base stations that support the 5GHz bands (all such systems also support the older bands). If you have ‘dead spots’ in your loft, consider a ‘mesh system’ base station with multiple transmitters.

* _Traffic_: as the amount of traffic people try to send over WiFi goes up, the amount of traffic each station can get through goes down. This means that WiFi throughput is only ever assured if you’re away from other WiFi systems and all other sources of interference (e.g. in the middle of the countryside). Otherwise you’re sharing radio waves.

So if you have systems in your loft that need reliable bandwidth, and/or are using a lot of network traffic, you’ll help yourself and your neighbors by using a wired connection for that traffic: you’ll get much better, more consistent, bandwidth, and your neighbors will experience less competition for the radio waves. I’d suggest that this is particularly a good idea for systems that use a lot of bandwidth but that do not move around. TVs, streaming boxes, and so on are typically fixed in place, and their streaming is bandwidth intensive. Most base stations have two ports – one to connect upstream to WebPass, and a wired ‘downstream’ port. in my loft I got lucky; my loft was wired by the previous occupants, so I connected a 18-port switch to my stations’s downstream port, and that enables me to hardwire all the static equipment and important places (e.g. my main desk where I do zoom calls) in my loft. An 8-port switch can be bought for [as little as $20](https://www.amazon.com/NETGEAR-8-Port-Gigabit-Ethernet-Unmanaged/dp/B07PFYM5MZ/ref=sr_1_3?th=1) and ethernet cables are also [cheap](https://www.amazon.com/Lysymixs-Ethernet-Centers-Network-Enterprise/dp/B0CY1PNCDY/ref=sr_1_5?th=1).

I don’t think WebPass will respond until we have shown that we have throughput problems that are *not* WiFi-related, i.e. someone does a bandwidth test when wired to the network, not using WiFi, and it shows problems.

(Yes, we all share the fiber coming from WebPass into our building, but the bandwidth available on an optical fiber is huge – we’re more likely limited by the throughput available on the wires from the mech room to each loft, than by competition for traffic on the fiber).
