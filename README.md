  ## Steps:-

   Note:- Please do it on your own risks.

    Download ISO
    Format USB flash drive as FAT32.
    Extract the ISO to the flash drive.
    Download UEFI shell: https://github.com/abhishekamralkar/uefi
    On the USB drive create a EFI folder and a BOOT sub folder, then copy Shell.efi to EFI\BOOT\Bootx64.efi
    Using a text editor, create a file called liveboot.nsh on the root of the USB drive and paste the following into the file:

           live\vmlinuz initrd=live\initrd.img append boot=live components live-media-path=/live

    Reboot PC and enter the UEFI Boot Menu, usually by pressing F8 or F12.
    Select the name of your USB flash drive (If you have CSM enanbled in BIOS you will see it twice, but one will have a UEFI: prefix, select that.).
    When EFI shell has loaded just type liveboot.nsh and press enter, it should then boot.
