# MDM-LIA
Modified Decrease Mechanism of LIA algorithm

## Introduction

Modified Decrease Mechanism of LIA algorithm (MDM-LIA) is a implementation of *a*STEAM Project <https://asteam.korea.ac.kr>. 
We have proposed `Dynamic congestion control algorithm for multipath TCP` <https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8539622> which indicated a modification in the *Linked Increases Algorithm* (LIA). Here we have modified the decrease mechanism of LIA, that means when any congestion or packet loss occurs we have decrease the congestion window dynamically in our proposed algorithm.

## Requirements and Dependencies

* The above development of our scheme was evaluated in network simulator `NS-3.13`.
* We have decreased the congestion window by multiplying by *beta* and *beta* is calculated by *gama* and balancing factor *delta* (0.25).
* Please add variables (`double Wmax`; `double pktLossTime`; `double Wrmax`; `double beta`;) to `mp-tcp-typedefs.h` file in `MpTcpSubFlow` class.

## Instructions

* The main modified code of decrease mechanism is in `mp-tcp-socket-base.cc` file. 

