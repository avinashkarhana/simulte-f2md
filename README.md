
Important Note
==============
As of 04/2022, the crownet project has completely switched to
[Simu5G](http://simu5g.org/) which is an improved model including
all components of SimuLTE. Therefore, we will no longer update
this fork of the SimuLTE project. We keep this repository only to
allow others to reproduce our results obtained with our fork
of SimuLTE.

For newer simulations, we recommend to use Simu5G.

The original Simu5G repository can be found at:

https://github.com/Unipisa/Simu5G

Thanks to the University of Pisa (Giovanni Nardini, Giovanni Stea, Antonio Virdis)
for making this great model publicly available.

For our Crownet project we maintain a slightly modified version of Simu5G
which can be found at:

https://github.com/roVer-HM/Simu5G



SimuLTE
=======

LTE/LTE-A user plane simulation model, compatible with the INET Framework.

Dependencies
------------

The current master/head version requires

- OMNeT++ 6.0pre12 and INET 4.3.3


Setup
-----

- PATH variable should include omnet bin directory and inet bin directory
- LIBRARY_PATH and LD_LIBRARY_PATH must include the location of the corresponding
shared object libraries 


Features
--------

General

- eNodeB and UE models
- Full LTE protocol stack

PDCP-RRC

- Header compression/decompression
- Logical connection establishment  and maintenance 

RLC

- Multiplexing/Demultiplexing of MAC SDUs
- UM, (AM and TM testing) modes

MAC

- RLC PDUs buffering
- HARQ functionalities (with multi-codeword support)
- Allocation management
- AMC
- Scheduling Policies (MAX C/I, Proportional Fair, DRR)

PHY

- Heterogeneous Net (HetNets) support: Macro, micro, pico eNbs
- Channel Feedback management
- Dummy channel model
- Realistic channel model with
  - inter-cell interference
  - path-loss
  - fast fading
  - shadowing 
  - (an)isotropic antennas

Other

- X2 communication support
- X2-based handover
- Device-to-device communications
- Support for vehicular mobility

Applications

- Voice-over-IP (VoIP)
- Constant Bit Rate (CBR)
- Trace-based Video-on-demand traffic


Limitations
-----------

- User Plane only (Control Plane not modeled)
- FDD only (TDD not supported)
- no EPS bearer support – note: a similar concept, "connections", has 
  been implemented, but they are neither dynamic nor statically 
  configurable via some config file
- radio bearers not implemented, not even statically configured radio 
  bearers (dynamically allocating bearers would need the RRC protocol, 
  which is Control Plane so not implemented)


