# Inverter-Design-and-Analysis-using-sky130pdk
### Design and Analysis of CMOS Inverter using the sky130 pdk and various open source tools
---

___I got busy and development has halted for a while. I plan to continue and complete this repo and would also welcome any contribution from others as well. Stay tuned for the bash script to install the tools for analog design flow(xschem+sky130pdk+ngspice+magic+netgen), that is in priority for now. Also special thanks to [Rajdeep](https://www.linkedin.com/in/rajdeep-mazumder/) for mentioning this repository in his videos, now I have a responsibility to manage it better which I am really excited for!!.___

---
This project has only one motive; that is to experiment with working of an inverter and understanding all the parameters involved with it. The design will utilise the models that are present under the __skywater 130nm pdk__ and various open source tools such as, __Xschem__, __NGSPICE__, __MAGIC__, __Netgen__, etc.

The whole process starts with analysis of _NMOS_ and _PMOS_ devices, specifically the 1.8v standard models available inside the pdk to determine a common working W/L ratio and also the gm, ron and similar values. After this we start with the design of a CMOS inverter that includes schematic, measurement of various parameters like delays, noise margin, risetime, falltime, etc. This part would also act as a case study on __SPICE__ where we use it's programming capabilities to better our abilities in measurements of aforementioned parameters. Then we will engage in the design a layout for our inverter in __magic layout editor__. Here, we will also explore the different layers available to the user and how we utilise them in a design and what it translates to in terms of a mask. Lastly, we compare the two netlists, that is the schematic and the layout one, which is popularly referred to as ___LVS___. If everything is hunky-dory, this project would then conclude. 

I will try to keep updating it as often as possible, as this first project is a primary resource for me to practice analog design, with the open source toolchain and definitely to keep a documentation that is easily understandable by anyone who later tries to practice it the same way.

Let's get right into it. 

## 2. Analysis of MOSFET models

### 2.1 General MOS Analysis

In this section I start with our analysis of MOSFET models present in sky130 pdk. I would be using the 1.8v transistor models, but you can definitely use and experiment with other ones present there. below is the schematic I created in **Xschem**.

___highly recommended to check out the tutorials of xschem [here](http://repo.hu/projects/xschem/xschem_man/xschem_man.html) and ngspice [here](http://ngspice.sourceforge.net/docs/ngspice-manual.pdf)___

![NMOS CHAR SCHEMATIC](./General_MOS_analysis/nfet_1v8.png)
