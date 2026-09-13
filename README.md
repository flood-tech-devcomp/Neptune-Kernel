# Neptune Open Source Kernel Project (NOSKP) 🪐

Welcome to the **Neptune Kernel**, a custom standalone x86 monolithic kernel written completely from scratch by one person using pure C and x86 Assembly. 

This project bypasses traditional operating system layers to talk directly to bare-metal simulation environments.

##  Current Features
- **Multiboot Implementation:** Boots smoothly from standard multiboot environments.
- **Remapped PIC Controllers:** Hardware interrupts mapped away from CPU system faults.
- **Custom Keyboard Driver:** Built an active Interrupt Descriptor Table (IDT) to process real hardware key inputs.
- **Clean Display Console:** Direct writing to legacy VGA text-mode memory maps (`0xB8000`).

## How to Compile 
Ensure you have `gcc`, `make`, and `qemu-system-x86` installed, then run:

```bash
cd ~/NOSKP
make clean && make
qemu-system-i386 -net none -kernel sysroot/neptune.bin
```
If you want to run it on windows you will need a 'fedora WSL' 'arch Linux WSL' or 'Ubuntu WSL'
