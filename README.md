# xiaomi notebook pro Tips
## bios flash & undervolt
with [_Cyb](http://en.miui.com/home.php?mod=space&do=thread&view=me&type=reply&uid=2250955959&from=space)‘s [patch](https://4pda.ru/forum/index.php?showtopic=843452&st=7960#entry75197781)(known from [reddit](https://www.reddit.com/r/Xiaomi/comments/93v6q6/mi_notebook_pro_bios_patcher_for_0502_and_0603/)) and [win系统一键刷BIOS](http://bbs.xiaomi.cn/t-14496063), we can **flash** bios 603, 502, 300  and **undervolt** in a super easy way

### how to

1. Download [voltagebios](https://raw.githubusercontent.com/tkkcc/minotebook/master/voltagebios.rar)
2. In folder `bios`, delete `TR100A04.fd`, rename `XMAKB5R0P0603.fd(or 502 300, the version you want)` to `TR100A04.fd`, run `H2OFFT-Wx64.exe` to flash, **it will automatically reboot several times**
3. With 300, undervoltage is not limited
4. With 603 or 502, go to folder `voltagepatch`, run `Patcher.cmd` by Administrator, reboot manually

> **Downgrade** is support, I flash 603 in 502 and flash back and flash back
> 
> The patch need **powershell** which doesn't exist in my lite win10, I finally successed with [Windows 10 (business editions), version 1803 (Updated Jul 2018) (x64)](ed2k://|file|cn_windows_10_business_edition_version_1803_updated_jul_2018_x64_dvd_12613133.iso|5075204096|9BE9662C6A1D206D4123556D743BC554|/) from [msdn.itellyou](https://msdn.itellyou.cn/)

Now use XTU in windows, and [intel-undervolt](https://github.com/kitsunyan/intel-undervolt) in linux to undervolt

## fan patch
_Cyb give [patchs](http://en.miui.com/forum.php?mod=viewthread&tid=1551743&page=16#pid29412725) which help increase fan temperatures thresholds, you can now keep the fan quiet

### how to

1. Download [patches](https://raw.githubusercontent.com/tkkcc/minotebook/master/patches.zip)
2. Follow the readme inside
> In order to let the EC read new firmware, I use 0% battery shutdown, the patch works after boot.

See also [xiaomi-notebook-pro-bios-patcher](https://github.com/saltukkos/xiaomi-notebook-pro-bios-patcher) for custom fan speed curve.  
See also [Mi-Notebook-Pro-Mods](https://github.com/Cr0wTom/Mi-Notebook-Pro-Mods) for new BIOS (805).  
All sources linked.  

## TLP

[TLP](https://wiki.archlinux.org/index.php/TLP) is a tool for better battery life on linux. I recommend trying my tlp [config](https://github.com/tkkcc/dot/blob/master/etc/default/tlp) without any performance loss. I can achieve more than 10 hours of 1080p video playing with mpv. Use [powerstat](https://aur.archlinux.org/packages/powerstat-git/) to measure temporal power consumption.
