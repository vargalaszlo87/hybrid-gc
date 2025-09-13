# hybrid-gc

## 🚀 What about is this project? 

This is a **gain control** circuit, where you can set the size of control voltage. What does it mean? 

❤️ If you would set the gain of this amplifier with DC voltage between 0 and 5V or between 0 and 0.5V, then you can easily make it. ❤️

## Short description

If you see this circuit for the first time, then seems simple. It includes some transistors, op amps and passive items. Seriously, the main part of this circuit is a common Emitter circuit with variable source resistance.

In this case the channel-resistance of FET (Rds) acts like a voltage controlled resistor. It's well know, the gain of the common-emitter amplifier depends strongly on the emitter resistance.

### Important task

Transfer characteristic of BF245A, see it:

<img width="613" height="595" alt="image" src="https://github.com/user-attachments/assets/495e7e7e-f73b-44d9-88ac-7a5ad7d8c64e" />

In this case the V_DS = 15V and the ambient temperature is 25°C.

**Approximately: How much is the channel-resistance?**

<img width="152" height="74" alt="image" src="https://github.com/user-attachments/assets/0647eddf-2355-4e23-a996-b777d0b1b8f6" />

Important thing: you cannot directly calculate RDS with this diagram. You need the size of the V_DS signal (The voltage difference between the drain and the source) at the point of V_GS voltage.

**Shockley equation**

<img width="297" height="104" alt="image" src="https://github.com/user-attachments/assets/4e19d81d-b88b-46fe-a5a5-78acc1ad2a9f" />

*In the case of BF245A:*

**V_p** = -2V
**I_dss** = 4mA

*See it my simulation:*

- The first V_GS value (at the point of 0V control voltage) is ca. -1.2V.
- I_d (V_GS = -1.2V) = 0.64mA
- The first V_DS value (at the point of 0V control voltage) is ca. 260mV.

The R_DS (at the point of 0V control voltage) = 0.26V / 0.00064mA = ~406ohm

At the point of 5V control voltage:

- V_GS = 0.18V
- I_D (V_GS = 0.1V) = ca. 4.75mA
- V_DS = 315mV

The R_DS (at the point of 5V control voltage) = 0.315V / 0.00475mA =  ~66ohm.

**So, we have a voltage controller resistor between 66ohm and 406ohm.**


