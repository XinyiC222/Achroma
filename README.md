# Achroma
Achroma is a wireless reversible split keyboard with 36 keys that is powered by ZMK. It uses a nine!nano v2 replica from aliexpress. There are two versions of Achroma, the Choc/Choc_v2 compatible one, and the MX compatible one! This is still a work in progress.
<img width="1041" height="353" alt="Screenshot 2026-08-30 at 11 53 14 AM" src="https://github.com/user-attachments/assets/326148d5-1d46-4c0e-b277-6b07cf525208" />
<img width="432" height="392" alt="Screenshot 2026-08-30 at 11 56 21 AM" src="https://github.com/user-attachments/assets/f6918ed5-c05c-42d6-a021-438333500752" /> (MX version)
<h1>Keymap</h1>
<img width="803" height="335" alt="Screenshot 2026-08-30 at 11 53 38 AM" src="https://github.com/user-attachments/assets/8e78507b-a0ae-4c13-b57d-9d2fc4faf985" />
<img width="804" height="344" alt="Screenshot 2026-08-30 at 11 53 43 AM" src="https://github.com/user-attachments/assets/fac5e366-53a6-465a-bbdf-8586f3a8b3a3" />
<img width="832" height="351" alt="Screenshot 2026-08-30 at 11 53 48 AM" src="https://github.com/user-attachments/assets/0452fd5d-9ea8-417f-8345-d0c81544de25" />

<h1>Resources</h1>
**Footprints and References:**
https://github.com/piit79/42keebs-kicad
https://flatfootfox.com/ergogen-part6-reversible-split/
https://github.com/kata0510/Lily58 (this has a great footprint library!)
https://github.com/aroum/PNCATEHO (reversible Choc footprints that fits both versions!)

**Tools**
https://www.keyboard-layout-editor.com/
https://nickcoutsos.github.io/keymap-editor/
https://github.com/adamws/kicad-kbplacer

<h1>Mini Guide/ My Process (Work in progress)</h1>
1. I first researched and wrote down what I wanted this project to look like at the end. Do I want it to be low profile or MX? Do I want this to be reversible? How much money do I want to spend on this? Do I want to make a custom layout, or do I want to use an existing one? Wireless? etc.
2. I ended up choosing to making my own layout and use ZMK for wireless. So I went ahead and looked for reversible footprints to use. I also wanted to use a battery for it. I then went into keyboard layout editor and made my desired layout.( I only made the left side first)
3. Then I created the schematics in kicad. It included a jst pin, a reversible nice!nano, choc/mx switches, LED, slide switch, and a reset button. 
4. then using the .json file from the layout I made in keyboard layout editor and the kbplacer, I organized the keys for the left split.
5. spent a lot of time between editing the schematics, the pcb, and testing new footprint libraries. After a ton of trial and error I made the general layout I wanted.
6. Exported the gerber files and imported them into jlc pcb.
7. I then added 3d models to each of the footprints and import it into fusion to make the case(MX only)
8. I looked for components in aliexpress
9. Then I started reading through how to set up ZMK and made the firmware using github actions.
10. Lastly once you've build the physical item, flash the firmware into the devices.
