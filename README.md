# Weather satellite radio project
During summer of 2020, when the state of the world was in lockdowm, I had come across a few videos which caught my eye. Talk of a way to grab and decode the data from a weather satellite, the NOAA satellites to be specific. Since I had always been quite interested in how the weather was monitored, and I had a love for astronomy I took it upon myself to try to decode even the smallest snippet of data from one of these satellites. Here I am after an entire year, if not more; finally with that small snippet of data to hand. 

## The crutial mistake and misunderstanding
After a small amount of research online I found out what I would need is an rtl-sdr and some kind of antenna to recieve the signal from the NOAA satellite, as well as some coaxial cable and a few connectors. An rtl-sdr is a very neat device which can be plugged into your computer and with the right software such as sdr sharp (sdr# for short), you would be able to listen to and monitor radio signals. For reference here is a list of what I bought to start with (these components are not the reason for the mistake made, that will be explained shortly):

- [Nooelec rtl-sdr (I found the mini version to have connection problems so I recommend this version)](https://www.amazon.co.uk/Nooelec-NESDR-SMArt-SDR-R820T2-Based/dp/B01HA642SW/ref=sr_1_2_sspa?keywords=Rtl+SDR&qid=1638297518&sr=8-2-spons&psc=1&smid=A1TIGMJ4AZ1K1A&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExR0xVWUhDRVdHNUlQJmVuY3J5cHRlZElkPUEwNTU1NDM1MVJJQUZDQU8xRjJIOCZlbmNyeXB0ZWRBZElkPUEwMjMzNTg3M1RaU1QyWVJQTUxQVSZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=)

- [Coaxial cable (I use 75 ohm but this 50 ohm is recommended)](https://www.amazon.co.uk/electrosmart-RG58-Black-Coaxial-Cable/dp/B01N5TR7OP/ref=sr_1_3?crid=CEK62CZO1H3H&keywords=50+ohm+coaxial+cable&qid=1638297676&sprefix=50+ohm+%2Caps%2C223&sr=8-3)

- [Coaxial female to SMA male connector](https://www.amazon.co.uk/Connector-Adaptor-Converter-Wireless-Instrumentation%EF%BC%88Pack/dp/B09B28LMTZ/ref=sr_1_5?keywords=female+coaxial+to+male+sma&qid=1638297872&sr=8-5)

- [Soldering iron and solder kit](https://www.amazon.co.uk/Soldering-Iron-Kit-Welding-Tools/dp/B09CPRJMSC/ref=sr_1_9?crid=2C3PJ98VBDOO0&keywords=soldering+iron&qid=1638298287&sprefix=soldering+iron%2Caps%2C171&sr=8-9)

This list of items may seem very short and in reality, it is. However, I decided to make some shortcuts when trialing a test run just to make sure the overall design was solid and to see whether it would work at all. One of the crutial components which isn't in this list is the antenna, and I will explain how I built a rough antenna to begin with. After searching around, taking a look at a few designs for antennas I decided to settle on a dipole. A dipole consists of two wires, each 53.4cm in length (in the case of focusing on the 137Mhz line), made out of copper or aluminium with a diameter 3mm. Since I didn't want to fully commit to building a dipole at first, I decided to build a rough one by stripping back the coaxial wires and using the copper core to build the dipole. I had cut out two 'poles' roughly 53.4cm in length and began soldering these two 'poles' to the core of the main coaxial wire which would connect to my rtl-sdr. ***Here is where the mistake was made. One of the poles should be soldered to the core of the coaxial wire whilst the other should be connected to the outer copper mesh of the coaxial wire in order to complete the circuit.*** On my first attempt I had soldered both the poles to the copper core instead of one to the core and the other to the copper mesh. As a result when the satellite passed overhead, all I could see was a static mess once decoded by wxtoimg (a very useful decoding program for NOAA satellites). [link](SatelliteRadio.html)
