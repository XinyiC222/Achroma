# Achroma
Achroma is a wireless reversible split keyboard with 36 keys that is powered by ZMK. It uses a nine!nano v2 replica from aliexpress. There are two versions of Achroma, the Choc/Choc_v2 compatible one, and the MX compatible one! This is still a work in progress. Theres only a case for the MX version. But there are two different pcb designs based on which one you want to use.
<img width="1041" height="353" alt="Screenshot 2026-08-30 at 11 53 14 AM" src="https://github.com/user-attachments/assets/326148d5-1d46-4c0e-b277-6b07cf525208" />
<img width="432" height="392" alt="Screenshot 2026-08-30 at 11 56 21 AM" src="https://github.com/user-attachments/assets/f6918ed5-c05c-42d6-a021-438333500752" /> (MX version)
<h1>Keymap</h1>
<img width="803" height="335" alt="Screenshot 2026-08-30 at 11 53 38 AM" src="https://github.com/user-attachments/assets/8e78507b-a0ae-4c13-b57d-9d2fc4faf985" />
<img width="804" height="344" alt="Screenshot 2026-08-30 at 11 53 43 AM" src="https://github.com/user-attachments/assets/fac5e366-53a6-465a-bbdf-8586f3a8b3a3" />
<img width="832" height="351" alt="Screenshot 2026-08-30 at 11 53 48 AM" src="https://github.com/user-attachments/assets/0452fd5d-9ea8-417f-8345-d0c81544de25" />

<h1>Resources</h1>
<h3>Footprints and References:</h3>

https://github.com/piit79/42keebs-kicad

https://flatfootfox.com/ergogen-part6-reversible-split/

https://github.com/kata0510/Lily58 (this has a great footprint library!)

https://github.com/aroum/PNCATEHO (reversible Choc footprints that fits both versions!)

<h3>Tools</h3>

https://www.keyboard-layout-editor.com/

https://nickcoutsos.github.io/keymap-editor/

https://github.com/adamws/kicad-kbplacer

<h1>Mini Guide/ My Process (Work in progress)</h1>

1. I first researched and wrote down what I wanted this project to look like at the end. Do I want it to be low profile or MX? Do I want this to be reversible? How much money do I want to spend on this? Do I want to make a custom layout, or do I want to use an existing one? Wireless? etc.
2. I ended up choosing to making my own layout and use ZMK for wireless. So I went ahead and looked for reversible footprints to use. I also wanted to use a battery for it. I then went into keyboard layout editor and made my desired layout.( I only made the left side first)
3. Then I created the schematics in kicad. It included a jst pin, a reversible nice!nano, choc/mx switches, LED, slide switch, and a reset button.
4. then using the .json file from the layout I made in keyboard layout editor and the kbplacer, I organized the keys for the left split.
5. spent a lot of time between editing the schematics, the pcb, and testing new footprint libraries. After a ton of trial and error I made the general layout I wanted.  <img width="669" height="581" alt="Screenshot 2026-08-14 at 11 48 46 PM" src="https://github.com/user-attachments/assets/d9c77be9-3df2-45ad-8046-b5981d78f557" />

6. Exported the gerber files and imported them into jlc pcb.
7. I then added 3d models to each of the footprints and import it into fusion to make the case(MX only) <img width="725" height="637" alt="Screenshot 2026-08-16 at 12 56 51 PM" src="https://github.com/user-attachments/assets/c5be81e1-61a5-4ea5-bbf2-6614a139f221" />

8. I looked for components in aliexpress
9. Then I started reading through how to set up ZMK and made the firmware using github actions.
10. Lastly once you've build the physical item, flash the firmware into the devices.
<img width="438" height="331" alt="Screenshot 2026-08-30 at 11 56 32 AM" src="https://github.com/user-attachments/assets/852533ed-ffd5-4c57-a3a8-59d902e629e9" />

<h1>BOM</h1>
Here's the BOM! The Quantity listed below are the amount they gave and some don't have enough for the project if you are using this as a reference. All listed items are required for the build and it is only the quantity column that you should be careful when referencing. EX. I only ordered hotswaps in a pack of 10 cause I have some at home

| Item | Purpose | Price | Quantity | Source |
| :--- | :--- | :--- | :--- | :--- |
| Nice!Nano V2.0 | Micro controller | $1.95 | 1 | Aliexpress |
| Nice!Nano V2.0 | Micro comtroller | $2.81 | 1 | Aliexpress |
| M2 6mm screws | securing the pcb | $1.37 | x50 | Aliexpress |
| M2xL3xOD3.2 heat inserts | for the screws | $0.99 | x100 | Aliexpress |
| Gateron Milky Switches | switches | $6.91 | x30 | Aliexpress |
| SK6812 MINI-E RGB | RGB | $3.61 | x100 | Aliexpress |
| Hotswap Sockets | sockets for switches | $1.33 | x10 | Aliexpress |
| Horizontal Microswitch | reset button | $2.04 | x50 | Aliexpress |
| PH 2.0 Horizontal Header Socket | for the battery | $1.80 | x10 | Aliexpress |
| SS12D00G3 Toggle Switch | battery on/off | $0.92 | x5 | Aliexpress |
| IN4148 SOD-123 | diodes | $2.08 | x100 | Aliexpress |
| 3.7V 2000mAh Polymer Lithium Battery | Battery | $9.23 | x2 | Aliexpress |
| PCB | connect everything together | $9.60 | x5 | JLCPCB |
| **Aliexpress Subtotal** | | **$35.48** | | |
| **JLC Subtotal** | | **$9.60** | | |
| **shipping+tax** | | **+$12.14** | | |
| **Total:** | | **$57.22** | | |
