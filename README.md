
<h1>BRAND NEW DIY TUTORIAL BY LEBIGMAC !<br>How to ROOT your boot.img with Magisk (for Samsung Galaxy S23 Ultra & more)</h1>

NOTE: For Android 13. Your bootloader needs to be unlocked for this procedure to work!


1) Download your device's firmware from the internet (check your firmware version in 'About phone' > 'Software version')

Extract and unlz4 both boot.img and init_boot.img files from your firmware

<code>unlz4 boot.img.lz4 boot.img</code>

Repeat this step for the other file as well. I have attached my original S23 Ultra files for your convenience ;)


2) Install the latest official Magisk on your phone. The one I included for your convenience is deprecated already and doesn't work properly! To make it kind of work you can go into Magisk settings and set toasts to 'none' and the prompt to 'grant'.

<code>adb install Magisk-v25.2.apk</code>


3) Patch both boot.img and init_boot.img inside Magisk app (click 'install' > 'select and patch file')


4) Rename both files to boot.img and init_boot.img respectively (the larger file should be your boot.img)
<code>adb shell "cd /sdcard/Download/; mv magisk_patched_*.img boot.img"</code>
<code>adb shell "cd /sdcard/Download/; mv magisk_patched_*.img init_boot.img"</code>


5) Tar both files with this command:
<code>adb shell "cd /sdcard/Download/; tar cvf boot_patched.tar boot.img init_boot.img"</code>


6) Pull the patched tar file from your device to your computer
<code>adb pull /sdcard/Download/boot_patched.tar</code>


7) Reboot phone into Download mode:
<code>adb reboot download</code>


8) Execute Odin as administrator in Windows and select your new boot_patched.tar in the AP slot


9) Flash it


10) Enjoy your rooted device :D


If you like my hard work please consider donating at the link below.
Thank you very much for your support!


Forever yours,
lebigmac


DOWNLOAD ATTACHMENT AT
http://www.systemrw.com
