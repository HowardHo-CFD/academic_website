---
title: "Bernoulli Equation Simulator - Pipe 🚰"
layout: "simple"
showDate: false
showReadingTime: false
showWordCount: false
build:
  list: never
---
{{< katex >}}

This interactive simulation visualizes fluid flow through a pipe to demonstrate **Bernoulli’s Principle**. For an incompressible, frictionless fluid, the total pressure along a continuous streamline remains perfectly constant.

This total pressure is the sum of three components:

\\(p + \frac{1}{2}\rho V^2 + \rho g z = \text{constant}\\)

* **Static Pressure** \\(p\\): The actual thermodynamic pressure of the fluid.
* **Dynamic Pressure** \\(\frac{1}{2}\rho V^2\\): The kinetic energy per unit volume.
* **Hydrostatic Pressure** \\(\rho g z\\): The potential energy per unit volume due to elevation.


Source Code: [Google Colab](https://colab.research.google.com/drive/1aIp_4nBYOLwCpgkYn2m8BlaLscH78vym?usp=sharing)

{{< bernoulli-pipe >}}