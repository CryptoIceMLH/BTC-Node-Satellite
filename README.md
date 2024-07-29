Bitaxe-Satellite


Free Open Source 
 
DECENTRALIZED COMMUNICATIONS
FOR BITCOIN HARDWARE


Hello BTC Tech Nerd Army!
My name is CryptoIce and I am a proud BTC tech nerd.
Thought you might want to join me on this journey into decentralization!


Research and Development into an integrated system that will allow a Bitaxe BTC miner to communicate two way via satellite with a public-pool.io remote instance.


Purpose is to decentralize Bitcoin mining communications by providing an alternative to centralized Internet Service providers.


Chapter1: Satellite
I am starting this mission by establishing communication via the geostationary satellite Es’hail-2 / QO-100.
The purpose for choosing an amateur satellite platform instead of amateur HAM radio for now is to avoid adding signal in space errors ( HF signal propagation is variable) whilst we get a working system integration between hardware and software.
QO-100 is in a geostationary orbit at 25.9° East ( 36182 Km over Africa ). It carries two “Phase 4” amateur radio transponders operating in the 2400 MHz and 10450 MHz bands. A 250 kHz bandwidth linear transponder intended for conventional analogue operations and an 8 MHz bandwidth transponder for experimental digital modulation schemes and DVB amateur television. In our case we will focus on the 250Khz narrow band.


Stage 1 objectives are as follows - Completed ( see twitter posts )
* Establish a Receive only connection with QO100 Satellite
* Lock on to the Satellite Beacon
* Establish a RX synch with satellite and download HTML website of satellites own live status page.



Receiving Test Data Video  (YouTube link)



Stage 2 objectives are as follows - (CURRENT STAGE)
* Build a 2.4Ghz Transmitter and associated radio components ( see list below )
* Establish a Transmit and Receive (full duplex) connection with QO100 Satellite
* Transmit a data file from my location UK to WantClue in Germany.


Stage 3 objectives are as follows - (To be firmed up in due course)
* Modify Bitaxe firmware to communicate via SSB_HighSpeed_Modem
* Modify Public Pool to to communicate via SSB_HighSpeed_Modem


Stage 4 objectives are as follows
* Bitaxe hashes and delivers successful shares to the pool via satellite only connection



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


BTC LN : cryptoice@walletofsatoshi.com 
BTC On chain: 347ePgUhyvztUWVZ4YZBmBLgTn8hxUFNeQ
