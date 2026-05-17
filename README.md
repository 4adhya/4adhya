<svg width="800" height="195" viewBox="0 0 800 195" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#0d1117"/>
      <stop offset="100%" stop-color="#090d13"/>
    </linearGradient>
    <linearGradient id="fillGrad" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#7c6ef5" stop-opacity="0.4"/>
      <stop offset="100%" stop-color="#7c6ef5" stop-opacity="0.01"/>
    </linearGradient>
    <clipPath id="chartClip">
      <rect x="46" y="16" width="740" height="150"/>
    </clipPath>
  </defs>

  <!-- Background -->
  <rect width="800" height="195" rx="12" fill="url(#bgGrad)"/>

  <!-- Grid lines -->
  <line x1="46" y1="30"  x2="786" y2="30"  stroke="#1a2030" stroke-width="0.7"/>
  <line x1="46" y1="56"  x2="786" y2="56"  stroke="#1a2030" stroke-width="0.7"/>
  <line x1="46" y1="82"  x2="786" y2="82"  stroke="#1a2030" stroke-width="0.7"/>
  <line x1="46" y1="108" x2="786" y2="108" stroke="#1a2030" stroke-width="0.7"/>
  <line x1="46" y1="134" x2="786" y2="134" stroke="#1a2030" stroke-width="0.7"/>
  <line x1="46" y1="160" x2="786" y2="160" stroke="#1a2030" stroke-width="0.7"/>

  <!-- Y-axis labels -->
  <text x="40" y="34"  font-family="monospace" font-size="9" fill="#334055" text-anchor="end">14</text>
  <text x="40" y="60"  font-family="monospace" font-size="9" fill="#334055" text-anchor="end">10</text>
  <text x="40" y="86"  font-family="monospace" font-size="9" fill="#334055" text-anchor="end">6</text>
  <text x="40" y="112" font-family="monospace" font-size="9" fill="#334055" text-anchor="end">4</text>
  <text x="40" y="138" font-family="monospace" font-size="9" fill="#334055" text-anchor="end">2</text>
  <text x="40" y="164" font-family="monospace" font-size="9" fill="#334055" text-anchor="end">0</text>

  <!--
    y-scale: 0 → y=160, 14 → y=30  =>  y = 160 - (val/14)*130
    x: 30 points, step = 740/29 ≈ 25.5, start x=46

    Point values (index: value):
    0:1  1:0  2:0  3:0  4:0  5:2  6:3  7:13  8:1  9:0
    10:1 11:0 12:0 13:0 14:0 15:0 16:5 17:2  18:3  19:0
    20:1 21:1 22:0 23:4 24:0 25:0 26:1 27:0  28:0  29:0

    y values:
    1→150.7  0→160  2→141.4  3→132.1  13→30  1→150.7  0→160
    1→150.7  0→160  0→160   5→113.6  2→141.4 3→132.1  0→160
    1→150.7  1→150.7  0→160  4→122.9  0→160   0→160
    1→150.7  0→160  0→160   0→160
  -->

  <!-- Points list (x, y):
    0:  46,     150.7
    1:  71.5,   160
    2:  97,     160
    3:  122.5,  160
    4:  148,    160
    5:  173.5,  141.4
    6:  199,    132.1
    7:  224.5,  30
    8:  250,    150.7
    9:  275.5,  160
    10: 301,    150.7
    11: 326.5,  160
    12: 352,    160
    13: 377.5,  160
    14: 403,    160
    15: 428.5,  160
    16: 454,    113.6
    17: 479.5,  141.4
    18: 505,    132.1
    19: 530.5,  160
    20: 556,    150.7
    21: 581.5,  150.7
    22: 607,    160
    23: 632.5,  122.9
    24: 658,    160
    25: 683.5,  160
    26: 709,    150.7
    27: 734.5,  160
    28: 760,    160
    29: 785.5,  160
  -->

  <!-- Fill area — fades in after line draws -->
  <g clip-path="url(#chartClip)">
    <polygon
      fill="url(#fillGrad)"
      opacity="0"
      points="46,150.7 71.5,160 97,160 122.5,160 148,160 173.5,141.4 199,132.1 224.5,30 250,150.7 275.5,160 301,150.7 326.5,160 352,160 377.5,160 403,160 428.5,160 454,113.6 479.5,141.4 505,132.1 530.5,160 556,150.7 581.5,150.7 607,160 632.5,122.9 658,160 683.5,160 709,150.7 734.5,160 760,160 785.5,160 785.5,160 46,160"
    >
      <animate attributeName="opacity" from="0" to="1" dur="1s" begin="2.4s" fill="freeze"/>
    </polygon>
  </g>

  <!-- Main animated line -->
  <polyline
    fill="none"
    stroke="#8b7ff5"
    stroke-width="2.2"
    stroke-linejoin="round"
    stroke-linecap="round"
    stroke-dasharray="2400"
    stroke-dashoffset="2400"
    points="46,150.7 71.5,160 97,160 122.5,160 148,160 173.5,141.4 199,132.1 224.5,30 250,150.7 275.5,160 301,150.7 326.5,160 352,160 377.5,160 403,160 428.5,160 454,113.6 479.5,141.4 505,132.1 530.5,160 556,150.7 581.5,150.7 607,160 632.5,122.9 658,160 683.5,160 709,150.7 734.5,160 760,160 785.5,160"
  >
    <animate attributeName="stroke-dashoffset" from="2400" to="0" dur="2.5s" begin="0.2s" fill="freeze" calcMode="spline" keyTimes="0;1" keySplines="0.4 0 0.2 1"/>
  </polyline>

  <!-- Dots — each fades in staggered after line finishes -->
  <circle cx="46"    cy="150.7" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="2.75s" fill="freeze"/></circle>
  <circle cx="71.5"  cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="2.80s" fill="freeze"/></circle>
  <circle cx="97"    cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="2.85s" fill="freeze"/></circle>
  <circle cx="122.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="2.90s" fill="freeze"/></circle>
  <circle cx="148"   cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="2.95s" fill="freeze"/></circle>
  <circle cx="173.5" cy="141.4" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.00s" fill="freeze"/></circle>
  <circle cx="199"   cy="132.1" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.05s" fill="freeze"/></circle>

  <!-- PEAK dot — larger, pulses continuously -->
  <circle cx="224.5" cy="30" r="4.5" fill="#c4baff" opacity="0">
    <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="3.1s" fill="freeze"/>
    <animate attributeName="r" values="4.5;7;4.5" dur="1.8s" begin="3.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="1;0.5;1" dur="1.8s" begin="3.5s" repeatCount="indefinite"/>
  </circle>
  <!-- Peak annotation line -->
  <line x1="224.5" y1="38" x2="224.5" y2="160" stroke="#4a3f9f" stroke-width="0.9" stroke-dasharray="3 3" opacity="0">
    <animate attributeName="opacity" from="0" to="0.7" dur="0.4s" begin="3.2s" fill="freeze"/>
  </line>
  <!-- Peak badge -->
  <rect x="196" y="16" width="58" height="16" rx="4" fill="#1c1838" opacity="0">
    <animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="3.2s" fill="freeze"/>
  </rect>
  <text x="225" y="28" font-family="monospace" font-size="9" fill="#c4baff" text-anchor="middle" opacity="0">
    peak · 13
    <animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="3.2s" fill="freeze"/>
  </text>

  <circle cx="250"   cy="150.7" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.15s" fill="freeze"/></circle>
  <circle cx="275.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.20s" fill="freeze"/></circle>
  <circle cx="301"   cy="150.7" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.25s" fill="freeze"/></circle>
  <circle cx="326.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.30s" fill="freeze"/></circle>
  <circle cx="352"   cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.35s" fill="freeze"/></circle>
  <circle cx="377.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.40s" fill="freeze"/></circle>
  <circle cx="403"   cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.45s" fill="freeze"/></circle>
  <circle cx="428.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.50s" fill="freeze"/></circle>
  <circle cx="454"   cy="113.6" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.55s" fill="freeze"/></circle>
  <circle cx="479.5" cy="141.4" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.60s" fill="freeze"/></circle>
  <circle cx="505"   cy="132.1" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.65s" fill="freeze"/></circle>
  <circle cx="530.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.70s" fill="freeze"/></circle>
  <circle cx="556"   cy="150.7" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.75s" fill="freeze"/></circle>
  <circle cx="581.5" cy="150.7" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.80s" fill="freeze"/></circle>
  <circle cx="607"   cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.85s" fill="freeze"/></circle>
  <circle cx="632.5" cy="122.9" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.90s" fill="freeze"/></circle>
  <circle cx="658"   cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="3.95s" fill="freeze"/></circle>
  <circle cx="683.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="4.00s" fill="freeze"/></circle>
  <circle cx="709"   cy="150.7" r="3.5" fill="#9d8ff7" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="4.05s" fill="freeze"/></circle>
  <circle cx="734.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="4.10s" fill="freeze"/></circle>
  <circle cx="760"   cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="4.15s" fill="freeze"/></circle>
  <circle cx="785.5" cy="160"   r="3"   fill="#5a50a8" opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.25s" begin="4.20s" fill="freeze"/></circle>

  <!-- X-axis labels -->
  <text x="46"    y="180" font-family="monospace" font-size="8.5" fill="#334055" text-anchor="middle">Apr 17</text>
  <text x="199"   y="180" font-family="monospace" font-size="8.5" fill="#334055" text-anchor="middle">Apr 23</text>
  <text x="352"   y="180" font-family="monospace" font-size="8.5" fill="#334055" text-anchor="middle">Apr 29</text>
  <text x="505"   y="180" font-family="monospace" font-size="8.5" fill="#334055" text-anchor="middle">May 6</text>
  <text x="658"   y="180" font-family="monospace" font-size="8.5" fill="#334055" text-anchor="middle">May 13</text>
  <text x="785.5" y="180" font-family="monospace" font-size="8.5" fill="#334055" text-anchor="middle">May 17</text>

  <!-- Title -->
  <text x="400" y="193" font-family="monospace" font-size="9" fill="#3d3060" text-anchor="middle">Aadhya Sharma · Contribution Graph</text>
</svg>| ✈️ **[Snippix](https://github.com/aadhyasharma)** | Travel collages app | Full-stack travel storytelling with user auth, content flows, and responsive UI |
| 🎓 **[Soclique](https://github.com/aadhyasharma)** | Student hub | React-based college society platform for event discovery and management |

<br/>

<img src="./assets/social.svg" width="800" alt="Connect"/>

</div>
