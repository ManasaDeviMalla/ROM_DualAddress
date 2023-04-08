# ROM_DualAddress
On-chip Dual Address ROM Design 

Consider an application, where the system ROM is required to supply two different data concurrently. This need can be fulfilled if the ROM is designed to have
dual address and dual data output. 

Two addresses are provided so that we may fetch two locations concurrently. The number of bits in the address bus will decide the number of locations in the ROM. Let us say that we provide 3 bits for the address and, therefore,
the ROM contains eight locations. Further, let us take data width as 64 bits. The
data that will be read from the ROM table are ‘dout1’ and ‘dout2’ corresponding
to the addresses, ‘addr1’ and ‘addr2’ respectively as shown in Figure 9.1. It should
be noted that the ROM content is only a single block of 8 × 64 bits even though
two addresses are involved in the design.

ROM size is 8 × 64 bits. Two locations, each of size 64 bits, can be accessed
and output to the data bus, ‘dout1’ and ‘dout2’ simultaneously using the two
addresses, ‘addr1’ and ‘addr2’ respectively.

 In order to match the speed of dual RAM,  which outputs the block of data delayed by two clock
cycles, we introduce two-stage pipelining in the dual ROM design. 
