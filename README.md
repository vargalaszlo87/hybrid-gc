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

Why is the transfer-characteristic so important? **Approximately: The channel-resistance is V_GS / I_D.

<img width="152" height="74" alt="image" src="https://github.com/user-attachments/assets/0647eddf-2355-4e23-a996-b777d0b1b8f6" />



