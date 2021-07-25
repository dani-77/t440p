# t440p
My T440p Coreboot rom

The x200_8mb_ukqwerty_vesafb.rom is a Libreboot rom.

The 1280_seabios_x200_8mb_vgarom_vesafb.rom is a Coreboot rom.

With coreboot or libreboot already flashed, flash using:
sudo flashrom -p internal -w nameofthe.rom -V

With stock bios, you should use an external flasher (Rpi, BBB or another). Find instructions at coreboot.org or libreboot.org or retroboot.org.
