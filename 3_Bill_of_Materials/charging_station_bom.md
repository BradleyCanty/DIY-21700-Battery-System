# Charging Station Bill of Materials
| Item | Quantity | Unit Cost | Total Cost | Notes |
| :--- | :--- | :--- | :--- | :--- |
| Black ASA filament | 0.5 kg | $10 | $10 | |
| Antispark PCB | 1 | $12 | $12 | Source from PCBWay or JLCPCB |
| Antispark components | (See BOM) | N/A | $18 | See antispark BOM<br>Source from DigiKey or Mouser |
| Charging Station PCB | 1 | $6.4 | $6.4 | Source from PCBWay or JLCPCB |
| JST-XH female M+1-pin connector w/ wires | 1 | $1.5 | $1.5 | M = # of cells in series |
| JST-XH male M+1-pin connector | 2 | $0.25 | $0.5 | M = # of cells in series |
| male 12-pin, 2.7 mm pitch blade connector | 1 | $4 | $4 | Model: MISTA MSD-DB01M-12P <br> Source from AliExpress |
| XT60 female connector | 1 | $0.5 | $0.5 | |
| Large clear shrink tube | 1 | $0.1 | $0.1 | Diameter = 27 mm<br>Length = 40 mm |
| Small clear shrink tube | 1 | $0.1 | $0.1 | Diameter = 12 mm<br>Length = 40 mm |
| Rounded dowel pins | Q | $0.5 | Q × $0.5 | Diameter = 6 mm <br> Length = 15 mm <br> M = # of cells in series<br>if M ≤ 8, then Q = 4<br>else, Q = 8 |
| 28 AWG wire, red | 10 cm | $0.1 | $0.1 | |
| 12 AWG wire, red | 20 cm | $0.2 | $0.2 | |
| 12 AWG wire, black | 20 cm | $0.2 | $0.2 | |
| M3 × 6 mm bolts | 4 | $0.1 | $0.4 | |

---

**Total cost** = `$54.0 + Q × 0.5`\
where\
**Q** = # of rounded dowel pins\
**M** = # of cells in series\
If `M ≤ 8` then `Q = 4`; else, `Q = 8`
