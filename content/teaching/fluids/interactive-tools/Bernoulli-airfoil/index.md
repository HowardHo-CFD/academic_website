---
title: "Bernoulli Equation Simulator - Airfoil  ✈"
layout: "simple"
showDate: false
showReadingTime: false
showWordCount: false
build:
  list: never
---
{{< katex >}}

This interactive simulation visualizes air flow over a symmetric wing (NACA 0012) to demonstrate **Bernoulli’s Principle** in aerodynamics. For an incompressible, frictionless fluid, the total pressure along a streamline remains constant.

💡 We are pretty certain a NACA0012 will stall when AOA is great than 20 degrees at any realistic Reynolds number, which is not reflected with the bernoulli equation. Therefore, the results need to be interpred with a bucket of salt at high AOA.


<!-- Source Code: [Google Colab](https://colab.research.google.com/drive/1aIp_4nBYOLwCpgkYn2m8BlaLscH78vym?usp=sharing) -->

{{< bernoulli-airfoil >}}