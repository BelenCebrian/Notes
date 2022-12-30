
# Info

- Opciones de desarrolladores ✔
	- USB Debugging ✔
- Platform Tools + ADB autorizado en Legion 5 Pro ✔
- Bootloader bloqueado ❌
- Oxygen OS 11 (actualizar a OOS 12 para [**Nameless ROM**]()❌
	- Instrucciones #1 (Web): https://nameless.wiki/getting-started/install/for_8_9R
	- Instrucciones #2 (Telegram): https://telegra.ph/Installation-instructions-07-23-2 

<br>

- **HOWTO** instalar el firmware en las dos particiones ([XDA](https://forum.xda-developers.com/t/rom-official-oos-cam-oneplus-8t-9r-12-1-0_r11-nameless-aosp-2022-07-23.4403295/page-51#post-87854995)):   
	- >When they say flash OOS12 both slots means, make sure you do update of OOS12 twice. Like update from oos11 to OOS12 is once, and update from oos12 to oos12 again is twice. By doing so, you are guaranteed to flash OOS12 on both slots. To flash from oos12 to oos12, on nameless wiki, they have apk to unlock such action. Read the instructions clearly. You will see apk.

	- >A little late on this, but Lineage OS has a zip that does it faster. Just sideload it in recovery and it does it all for you. This works for every rom I've tried, not just LOS: <https://mirrorbits.lineageos.org/tools/copy-partitions-20220613-signed.zip>

<br>
# Herramientas

1. Nameless: [XDA](https://forum.xda-developers.com/t/rom-official-oos-cam-oneplus-8t-9r-12-1-0_r11-nameless-aosp-2022-07-23.4403295/) | [HTCMania](https://www.htcmania.com/showthread.php?t=1630768)
1.  Fastboot Enhance: [XDA](https://forum.xda-developers.com/t/tool-windows-fastboot-enhance-payload-dumper-image-flasher.4310553/)
<br>

- Tipo de RAM ([Hilo XDA](https://forum.xda-developers.com/t/rom-stock-fastboot-stock-oxygenos-fastboot-roms-for-oneplus-8t.4348023/)): 

```RAM
adb shell getprop ro.boot.ddr_type
```

>0
  
- **0 = LPDDR4X** ✔
- **1 = LPDDR5**