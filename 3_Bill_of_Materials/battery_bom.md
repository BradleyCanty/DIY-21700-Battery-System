# Battery Bill of Materials
| Item | Quantity | Unit Cost | Total Cost | Notes |
| :--- | :--- | :--- | :--- | :--- |
| Black ASA | 0.5 kg | $10 | $10 | |
| White ASA | 0.25 kg | $5 | $5 | |
| Torsion spring | 4 | $0.5 | $2 | 1.2 mm × 10 mm × 3 laps × 120° |
| Small dowel pin | 4 | $0.1 | $0.4 | Diameter = 3 mm <br> Length = 12 mm |
| 21700 cell | M × N | C | M × N × C | M = # of cells in series<br>N = # of cells in parallel |
| Battery PCB | 1 | $6.4 | $6.4 | |
| M3 × 4 mm × 5 mm brass threaded insert nut | 16 | $0.1 | $1.6 | |
| 8 AWG black wire | 10 cm | $1 | $1 | |
| 8 AWG red wire | 10 cm | $1 | $1 | |
| 14 AWG bare copper wire | 20 cm | $2 | $2 | |
| Female 12-pin, 2.7 mm pitch blade connector | 1 | $4 | $4 | Model: MISTA MSD-DB01F-12P |
| 6 mm male bullet connector | 2 | $0.25 | $0.5 | |
| 6 mm female bullet connector | 2 | $0.25 | $0.5 | |
| JST-XH M+1-pin connector w/ wires | 1 | $1.5 | $1.5 | M = # of cells in series |
| M3 × 3 mm × 5 mm brass threaded insert nut | 2 | $0.1 | $0.2 | |
| M3 × 16 mm bolt | 8 + Q | $0.1 | $0.8 + $0.1 × Q | if N = 3, Q = 0; else Q = 4 |
| M3 × 12 mm bolt | 4 | $0.1 | $0.4 | |
| M3 × 6 mm bolt | 4 | $0.1 | $0.4 | |
| M3 × 5 mm bolt | 4 - Q | $0.1 | $0.4 - $0.1 × Q | if N = 3, Q = 0; else Q = 4 |
| Nickel-plated copper strip | S | $25.5 | $25.5 × S | Source from AliExpress<br>cell-to-cell distance = 22.5 mm<br>2p strip: each strip has 36 terminals along its length<br>S = ⌈M × N / 36⌉<br>e.g. if config. is 8s5p then M = 8 & N = 5<br>S = ⌈8 × 5 / 36⌉ = ⌈40 / 36⌉ = ⌈1.111⌉ = 2 |
---

**Total Cost** = `$38.5 + (M × N × C) + ($25.5 × S)`\
where\
**M** = # of cells in series\
**N** = # of cells in parallel\
**C** = unit cost of chosen 21700 cell\
**S** = `⌈(M × N) / 36⌉`
