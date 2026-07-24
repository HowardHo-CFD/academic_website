---
title: "Surface Tension Simulator - Droplet 💧"
layout: "simple"
showDate: false
showReadingTime: false
showWordCount: false
build:
  list: never
---
{{< katex >}}


Use the slider to adjust the contact angle \\(\theta\\) and observe how surface wetting behavior changes from wetting (\\(\theta < 90^\circ\\)) to non-wetting (\\(\theta > 90^\circ\\)). The vectors at the contact points represent the three surface tension forces in Young's equation: \\(F_{\sigma, SG}\\) (solid–gas), \\(F_{\sigma, SL}\\) (solid–liquid), and \\(F_{\sigma,LG}\\) (liquid–gas, acting tangent to the droplet surface). At equilibrium, the horizontal force balance along the solid surface satisfies Young's equation: \\(F_{\sigma,SG} = F_{\sigma,SL} + F_{\sigma,LG} \cos\theta\\)

Source Code: [Google Colab](https://colab.research.google.com/drive/1aIp_4nBYOLwCpgkYn2m8BlaLscH78vym?usp=sharing)

{{< droplet >}}