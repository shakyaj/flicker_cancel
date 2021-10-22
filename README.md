# SSCS PICO project (USA-1) - novel flicker noise cancellation technique in SKY130 technology

## table of contents
1. Project description
2. Schematic and test setup 
3. Layout (til date)
4. Noise simulation

A flicker noise cancellation technique using bias-switching technique is proposed. In this scheme instead of chopping the input, the effective Gm is switched from +Gm to -Gm periodically by switching bias current. This has several benefits over traditional chopping technique such as:
1. The input stays high impedance and there is no need to have a driver or buffer to connect to such circuit block.
2. The chopping glitches and transients are all common mode and hence chopping artifacts is reduced.
3. A continuous time signal can be passed through such circuit block without sampling. For example proposed Gm can be used for Gm-C integrator and hence benefit from sampling at the output of the Gm-C integrator and hence reducing input referred kT/C noise.
4. Allows for trading power for reducing flicker noise. Conventionally only device size can be increased to reduce the flicker noise. Increasing current increases flicker noise in conventional design.

Figure below shows the schematic of the proposed flicker noise cancelled Gm in pushpull structure.
![schematic](figures/gm_noflicker_schematic.png)  

