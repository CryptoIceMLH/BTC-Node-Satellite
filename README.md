Bitaxe-Satellite
Free Open Source
DECENTRALIZED COMMUNICATIONS
FOR BITCOIN HARDWARE

Hello BTC Tech Nerd Army!

My name is CryptoIce and I am a proud BTC tech nerd. Thought you might want to join me on this journey into decentralization!

![BTC spartan](https://github.com/user-attachments/assets/b2f0130b-c58c-424d-8f9e-ec5d41c32a43)

Research and Development into an integrated system that will allow a Bitaxe BTC miner to communicate two way via satellite with a public-pool.io remote instance.

Purpose is to decentralize Bitcoin mining communications by providing an alternative to centralized Internet Service providers.

Chapter1: Satellite

I am starting this mission by establishing communication via the geostationary satellite Es’hail-2 / QO-100.

The purpose for choosing an amateur satellite platform instead of amateur HAM radio for now is to avoid adding signal in space errors ( HF signal propagation is variable) whilst we get a working system integration between hardware and software.

QO-100 is in a geostationary orbit at 25.9° East ( 36182 Km over Africa ). It carries two “Phase 4” amateur radio transponders operating in the 2400 MHz and 10450 MHz bands. A 250 kHz bandwidth linear transponder intended for conventional analogue operations and an 8 MHz bandwidth transponder for experimental digital modulation schemes and DVB amateur television. In our case we will focus on the 250Khz narrow band.

![eshail-footprint](https://github.com/user-attachments/assets/ddb29a05-e179-420b-9681-51a40983b3b7)

Stage 1 objectives are as follows - Completed ( see twitter posts )

-Establish a Receive only connection with QO100 Satellite

-Lock on to the Satellite Beacon

-Establish a RX synch with satellite and download HTML website of satellites own live status page.

![IMG_20240702_120258](https://github.com/user-attachments/assets/3eebef35-47fb-461c-8809-0bafb4168424)
![IMG_20240722_142157](https://github.com/user-attachments/assets/d0a7155a-19e3-4a63-8243-1d3b54705f67)
![IMG_20240723_213417](https://github.com/user-attachments/assets/bcbf63e0-101d-48f2-bd1e-bf9f00785eb1)
![IMG_20240708_014524](https://github.com/user-attachments/assets/6cb711ba-01f2-4382-8b3b-377accd2c297)
![trak](https://github.com/user-attachments/assets/d83b20f4-9870-49fc-af68-b958d59354e4)
![omfg](https://github.com/user-attachments/assets/6e2d8163-4547-45fa-b98c-b47da373537a)

youtube.com/watch?v=og5Qzyo06EI

Stage 2 objectives are as follows - (CURRENT STAGE)

-Build a 2.4Ghz Transmitter and associated radio components ( see list below )

-Establish a Transmit and Receive (full duplex) connection with QO100 Satellite

-Transmit a data file from my location UK to WantClue in Germany.



Stage 3 objectives are as follows - (To be firmed up in due course)

-Modify Bitaxe firmware to communicate via SSB_HighSpeed_Modem

-Modify Public Pool to to communicate via SSB_HighSpeed_Modem



Stage 4 objectives are as follows

-Bitaxe hashes and delivers successful shares to the pool via satellite only connection



Current Status

Stage 1 has been successfully completed, all Receiving hardware has been build and data was downloaded as expected.

Stage 2 is now underway, starting with preparing a list of hardware required in order to built the required transmitter. As it seems sending data back up to 36182Km take a little bit more effort than just receiving. Below is the BOM for the Transmitter hardware needs.

1)Pluto+ SDR - $250

2)Analogue devices CN0417 pre-amplifier $50

3)Bias-T network - $30

4)Bullseye LNB - $40

5)105cm offset dish - $60

6)2.4Ghz ConeFeed Tx uplink antenna - $130

7)SG Labs 2.4GHz power amplifier - $150

8)DC-DC conveter for 20W power amplifier - $20

9)DC-DC converter for Pluto+ and pre-amplifier - $20

Total = $750


This is a wild time we live in, I want BTC to be prepared for all possible attack vectors.. that includes loss on centralized Coms !
With your continued support I can expedite the R&D process and deliver results in an expedited manor. 

BTC LN : cryptoice@walletofsatoshi.com BTC Onchain: 347ePgUhyvztUWVZ4YZBmBLgTn8hxUFNeQ
