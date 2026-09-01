# Achroma

Achroma is a wireless reversible split keyboard with 36 keys that is powered by ZMK. It uses a nine!nano v2 replica from aliexpress. There are two versions of Achroma, the Choc/Choc_v2 compatible one, and the MX compatible one! This is still a work in progress. Theres only a case for the MX version. But there are two different pcb designs based on which one you want to use. Here is the ZMK source files: https://github.com/XinyiC222/zmk-achroma-config I made this after seeing countless split keyboard builds that people where making online and I wanted to join in on the fun! To use it you just have to turn on the on/off button that is connected to the battery. The pcb is designed in kicad and the case is modeled in Fusion360.

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

Fusion360

Kicad

<h1>Mini Guide/ My Process (Work in progress)</h1>

Before starting, you should have already made some kind of electronic project prior to this. It would come off easier if you've designed a pcb before. Reading guides you find online can be super helpful. there are many resources that I didn't link but anything online is helpful. 

1. I first researched and wrote down what I wanted this project to look like at the end. Do I want it to be low profile or MX? Do I want this to be reversible? How much money do I want to spend on this? Do I want to make a custom layout, or do I want to use an existing one? Wireless? etc.
2. I ended up choosing to making my own layout and use ZMK for wireless. So I went ahead and looked for reversible footprints to use. I also wanted to use a battery for it. I then went into keyboard layout editor and made my desired layout.( I only made the left side first)
3. Then I created the schematics in kicad. It included a jst pin, a reversible nice!nano, choc/mx switches, LED, slide switch, and a reset button.
4. then using the .json file from the layout I made in keyboard layout editor and the kbplacer, I organized the keys for the left split.
5. spent a lot of time between editing the schematics, the pcb, and testing new footprint libraries. After a ton of trial and error I made the general layout I wanted.  <img width="669" height="581" alt="Screenshot 2026-08-14 at 11 48 46 PM" src="https://github.com/user-attachments/assets/d9c77be9-3df2-45ad-8046-b5981d78f557" />

6. Exported the gerber files and imported them into jlc pcb.
7. I then added 3d models to each of the footprints and import it into fusion to make the case(MX only) <img width="725" height="637" alt="Screenshot 2026-08-16 at 12 56 51 PM" src="https://github.com/user-attachments/assets/c5be81e1-61a5-4ea5-bbf2-6614a139f221" />

8. I looked for components in aliexpress
9. Then I started reading through how to set up ZMK and made the firmware using github actions.
10. After you assemble the pcb and have printed the case out, use a M2 heat insert on all the holes in the case(5 total). Then place the pcb on top and use a M2 screw to tighten it in place.
11. Once you've build the physical item, flash the firmware into the devices. You can learn more about it in the ZMK docs. If you'll like to use the firmware provided, please head to the Firmware folder to download what i have for both the left and the right side.
<img width="438" height="331" alt="Screenshot 2026-08-30 at 11 56 32 AM" src="https://github.com/user-attachments/assets/852533ed-ffd5-4c57-a3a8-59d902e629e9" />

<h1>Schematic</h1>
<img width="781" height="489" alt="Screenshot 2026-09-01 at 12 18 42 PM" src="https://github.com/user-attachments/assets/9c151edd-c996-4d7d-88f3-e99ec2bb097b" />

<PCB>
<img width="697" height="619" alt="Screenshot 2026-09-01 at 12 19 13 PM" src="https://github.com/user-attachments/assets/731080f0-56e3-42e8-a729-d18db2552c62" />
<img width="718" height="523" alt="Screenshot 2026-09-01 at 12 19 52 PM" src="https://github.com/user-attachments/assets/d003cbd7-0e88-4ff0-929a-9da6e15d31fd" />
<img width="689" height="604" alt="Screenshot 2026-09-01 at 12 19 33 PM" src="https://github.com/user-attachments/assets/57204159-df68-4dba-b66e-cddc072c63d5" />
<img width="735" height="573" alt="Screenshot 2026-09-01 at 12 20 06 PM" src="https://github.com/user-attachments/assets/01d836ae-e534-4e7c-9256-959e7f269abb" />


<h1>BOM</h1>

Here's the BOM! The Quantity listed below are the amount you need. The links included come in bulks and vary depending on how much you are buyinh. All listed items are required for the build.

| Item | Purpose | Price | Quantity | Source |
| :--- | :--- | :--- | :--- | :--- |
| Nice!Nano V2.0 | Micro controller | $1.95 | 1 | [Aliexpress](https://www.aliexpress.com/item/3256812809465916.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%2010.84%21USD%203.25%21%21USD%203.25%21%21%21%402101dedf17882176157074667e0e98%2112000059988282797%21ct%21US%217294405090%21%211%210%21) |
| Nice!Nano V2.0 | Micro controller | $2.81 | 1 | [Aliexpress](https://www.aliexpress.com/item/3256807196955871.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%202.81%21USD%202.64%21%21USD%202.64%21%21%21%402101dedf17882176246834968e0e98%2112000047100969961%21ct%21US%217294405090%21%211%210%21) |
| M2 6mm screws | securing the pcb | $1.37 | x10 | [Aliexpress](https://www.aliexpress.com/item/3256807033160325.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%201.37%21USD%201.37%21%21USD%201.37%21%21%21%402101dedf17882176157074667e0e98%2112000039933522857%21ct%21US%217294405090%21%211%210%21) |
| M2xL3xOD3.2 heat inserts | for the screws | $0.99 | x10 | [Aliexpress](https://www.aliexpress.com/item/3256806651793931.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%203.08%21USD%200.99%21%21USD%200.99%21%21%21%402101dedf17882176157074667e0e98%2112000038467725083%21ct%21US%217294405090%21%211%210%21) |
| Gateron Milky Switches | switches | $6.91 | x36 | [Aliexpress](https://www.aliexpress.com/item/3256803874880557.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%207.35%21USD%206.91%21%21USD%206.91%21%21%21%402101dedf17882176157074667e0e98%2112000027903926419%21ct%21US%217294405090%21%211%210%21) |
| SK6812 MINI-E RGB | RGB | $3.61 | x36 | [Aliexpress](https://www.aliexpress.com/item/3256807677321116.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%203.61%21USD%203.61%21%21USD%203.61%21%21%21%402101dedf17882176246834968e0e98%2112000042594617264%21ct%21US%217294405090%21%211%210%21) |
| Hotswap Sockets | sockets for switches | $1.33 | x36 | [Aliexpress](https://www.aliexpress.com/item/3256807045726008.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%202.66%21USD%201.33%21%21USD%201.33%21%21%21%402101dedf17882176157074667e0e98%2112000039893759771%21ct%21US%217294405090%21%211%210%21) |
| Horizontal Microswitch | reset button | $2.04 | x2 | [Aliexpress](https://www.aliexpress.com/item/3256806318779497.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%202.04%21USD%202.04%21%21USD%202.04%21%21%21%402101dedf17882176246834968e0e98%2112000037444053760%21ct%21US%217294405090%21%211%210%21) |
| PH 2.0 Horizontal Header Socket | for the battery | $1.80 | x2 | [Aliexpress](https://www.aliexpress.com/item/3256808824951678.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%201.80%21USD%201.80%21%21USD%201.80%21%21%21%402101dedf17882176293735149e0e98%2112000047583383492%21ct%21US%217294405090%21%211%210%21&pdp_ext_f=%7B%22cart2PdpParams%22%3A%7B%22pdpBusinessMode%22%3A%22retail%22%7D%7D) |
| SS12D00G3 Toggle Switch | battery on/off | $0.92 | x2 | [Aliexpress](https://www.aliexpress.com/item/3256808561935510.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%200.92%21USD%200.92%21%21USD%200.92%21%21%21%402101dedf17882176319215275e0e98%2112000046504078875%21ct%21US%217294405090%21%211%210%21) |
| IN4148 SOD-123 | diodes | $2.08 | x36 | [Aliexpress](https://www.aliexpress.com/item/2255800498728983.html?spm=a2g0o.cart.0.0.564238daJS0mQo&mp=1&pdp_npi=6%40dis%21USD%21USD%202.08%21USD%202.08%21%21USD%202.08%21%21%21%402101dedf17882176365865480e0e98%2112000037997014577%21ct%21US%217294405090%21%211%210%21) |
| 401030 3.7V 110mAh Polymer Lithium Battery | Battery | $9.72 | x2 | [Aliexpress](https://www.aliexpress.us/item/3256811360999976.html?mp=1&pdp_npi=6@dis!USD!USD+11.30!USD+9.72!!USD+9.72!!!@210328df17882265747402256e0fd1!12000055885084344!ct!US!7294405090!!1!0!&gatewayAdapt=glo2usa) |
| PCB | connect everything together | $9.60 | x2 | JLCPCB |
| **Aliexpress Subtotal** | | **$36.66** | | |
| **JLC Subtotal** | | **$9.60** | | |
| **shipping+tax** | | **+$12.24** | | |
| **Total:** | | **$58.50** | | |
