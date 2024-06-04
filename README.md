# How to install Mac Sonoma in VMWare virtual machine

Navigate to this official Mac URL to learn more about **Sonoma Operating System (OS)**: 

https://www.apple.com/macos/sonoma/

See this youtube video: INSTALAR VMWARE WORKSTATION PRO O FUSION GRATIS 100% LEGAL [2024]

https://www.youtube.com/watch?v=Nvzb2spWGW0

See also this web page for a detailed explanation about **VMWare WorStation 17 and Fusion 13 FREE for Personal Use**

https://blogs.vmware.com/teamfusion/2024/05/fusion-pro-now-available-free-for-personal-use.html

For a general explanation about all the steps to create a **Mac Sonoma Virtual Machine (VMWare) in your Windows laptop** see this video: 

https://www.youtube.com/watch?v=h8oLSDUxDEw&t=857s

## Summary

- Downlaod/Install VMWare WorkStation 17 Pro

- Download Mac Sonoma iso image

- Unlock VMWare for Mac

- Create/Configure VMWare Virtual Machine for Mac Sonoma

- (OPTIONAL) Install VMWare Tools in Mac Sonoma for increasing the screen resolution

## 1. How to download/install VMWare WorkStation 17 Pro

We have to creat a new account in **Broadcom**

https://www.broadcom.com/

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/75269a1c-6543-4198-9226-9c9ee4470baa)

We have to follow this link to download the VMWare WorStation 17 Pro for personal use

https://support.broadcom.com/group/ecx/productdownloads?subfamily=VMware+Workstation+Pro

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/4443bd82-e817-4c90-9173-1e3c8c4adb06)


## 2. Download Mac Sonoma iso

See this video "How to Download macOS 14 Sonoma ISO File":

https://www.youtube.com/watch?v=cxJkQEro4lk

Follow this URL link to **download Mac Sonoma ISO**

https://drive.google.com/file/d/1FdocBt9nSuqGmNWpwkIWqXi7FbuBd8P3/view

This is the code for creating the ISO

```
hdiutil create -o /tmp/Sonoma -size 16384m -volname Sonoma -layout SPUD -fs HFS+J

hdiutil attach /tmp/Sonoma.dmg -noverify -mountpoint /Volumes/Sonoma

sudo /Applications/Install\ macOS\ Sonoma.app/Contents/Resources/createinstallmedia --volume /Volumes/Sonoma –nointeraction

hdiutil eject -force /Volumes/Install\ macOS\ Sonoma

hdiutil convert /tmp/Sonoma.dmg -format UDTO -o ~/Desktop/Sonoma

mv -v ~/Desktop/Sonoma.cdr ~/Desktop/Sonoma.iso

rm -fv /tmp/Sonoma.dmg
```

## 3. How to unlock VMWare for Mac

As prerequisite we first have to install the **VMWare WorkStation 17 Pro** in our laptop, as explained in section 1 in this document

We unzip the file **Unlocker-v2.0.1-x64.zip** in this github repo and press the **Patch** button

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/cf1c5855-86e2-4f67-9bc8-829b3a896987)

In the next section we can verify the Mac Virtual Machines are available in VMWare WorkStation Pro 17

## 3. Create/Configure Mac Sonoma Virtual Machine (with VMWare WorkStation Pro 17)

We create a new Virtual Machine(VM)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/f94271be-f8f1-4c8a-81ba-b8acd46dcbc5)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/1be9a4da-3266-444f-8e60-03590ddc295b)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/845a33d2-50c7-455c-bf4e-efcbf138a72f)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/1bce6942-9c1b-4388-a178-b6d351e585d2)

We configure the VM Ram memory. It is advisable to select minimum 8 Gb

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/64f68232-274f-4334-a5fe-aacb10ec0dac)



## 4. 


## 5. 



