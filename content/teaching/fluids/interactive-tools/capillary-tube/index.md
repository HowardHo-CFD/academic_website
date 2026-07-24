---
title: "Surface Tension Simulator - Capillary Tube 🧪"
layout: "simple"
showDate: false
showReadingTime: false
showWordCount: false
build:
  list: never
---
{{< katex >}}

Use the sliders to adjust the contact angle \\(\theta\\) and select different liquids to observe capillary rise vs. depression. The  <span style="color: #761e8a; font-weight: bold;">purple arrow</span> arrows represent the surface tension force \\(F_\sigma\\) along the contact line, while the  <span style="color: #e21010; font-weight: bold;">red arrow</span> represents the net gravity/hydrostatic pressure balance force \\(\gamma \pi R^2 h\\).

💡 Note: The column height vector \\(\vec{h}\\) is measured relative to the external reservoir level. When \\(\theta > 90^\circ\\) (e.g., Mercury), \\(\vec{h}\\) becomes negative and the net force vector flips upward.

<!-- Source Code: [Google Colab](https://colab.research.google.com/drive/1aIp_4nBYOLwCpgkYn2m8BlaLscH78vym?usp=sharing) -->

{{< capillary-tube >}}