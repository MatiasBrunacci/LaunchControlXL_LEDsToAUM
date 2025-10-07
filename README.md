# LaunchControlXL_LEDsToAUM

This is an **extended version** of the [Launch Control XL LEDs](https://patchstorage.com/launch-control-xl-leds/) Mozaic script originally shared by [richtowns](https://patchstorage.com/launch-control-xl-leds/).  
It adds **support for User Templates** (e.g. *User 1*, *User 2*, etc.), allowing you to use your own custom mappings while keeping full LED and ring feedback working in **AUM**.

The script forces the Launch Control XL to switch to the selected **User or Factory template** on load, then updates all button LEDs and knob rings in real time.  
It works in **Low Power Mode** directly connected to the iPad, and is ideal for controlling AUM or other iOS apps that can send and receive MIDI feedback.

---

### ✨ Features

- ✅ Compatible with **User and Factory templates**
- 🔄 **LED and ring feedback** fully functional
- ⚙️ Uses Mozaic’s `SendSysex` to communicate with the Launch Control XL
- 🧠 Simple variable `template = 0x00` lets you quickly switch between User/Factory modes
- 🧩 Drop-in replacement for [richtowns’ original patch](https://patchstorage.com/launch-control-xl-leds/)

---

### 🧰 Usage

1. Load this script in **Mozaic** inside **AUM**.  
2. Connect your **Launch Control XL** to **Mozaic** as both MIDI input and output.  
3. Edit the variable "template" `template = 0x00` to match your preferred template/preset:

- 0x00 → User 1
- 0x01 → User 2
- 0x02 → User 3
- 0x03 → User 4
- 0x04 → User 5
- 0x05 → User 6
- 0x06 → User 7
- 0x07 → User 8

- 0x08 → Factory 1
- 0x09 → Factory 2
- 0x10 → Factory 3
- 0x11 → Factory 4
- 0x12 → Factory 5
- 0x13 → Factory 6
- 0x14 → Factory 7
- 0x15 → Factory 8


Reload the script. The LCXL will switch to the chosen template and keep LED/ring feedback active.

---

🧠 Technical Notes

- Uses SysEx messages:
  - 0x77 → Change current template
  - 0x78 → Set LED/ring value
- Fully compatible with Launch Control XL in Low Power Mode on iPad.
- Tested in AUM on iPad OS 26+.

---

🙏 Credits

Original concept and base code by [richtowns](https://patchstorage.com/launch-control-xl-leds/).
