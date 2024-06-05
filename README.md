# How to install Mac Sonoma in VMWare virtual machine

## Hardware Prerequisite

This sample was developed with **HP Intel EVO i7 (12th Gen Intel(R) Core(TM) i7-1260P 2.10 GHz) 16.0 GB Ram** with these technical features:

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/bf87e5a0-5fee-43c4-94b7-a347ba32878e)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/05a19308-9135-4611-93f8-520c29ce1268)

## Summary

- Downlaod/Install VMWare WorkStation 17 Pro

- Download Mac Sonoma iso image

- Unlock VMWare for Mac

- Create/Configure VMWare Virtual Machine for Mac Sonoma

- (OPTIONAL) Install VMWare Tools in Mac Sonoma for increasing the screen resolution

## Additional information

Navigate to this official Mac URL to learn more about **Sonoma Operating System (OS)**: 

https://www.apple.com/macos/sonoma/

See this youtube video: INSTALAR VMWARE WORKSTATION PRO O FUSION GRATIS 100% LEGAL [2024]

https://www.youtube.com/watch?v=Nvzb2spWGW0

See also this web page for a detailed explanation about **VMWare WorStation 17 and Fusion 13 FREE for Personal Use**

https://blogs.vmware.com/teamfusion/2024/05/fusion-pro-now-available-free-for-personal-use.html

For a general explanation about all the steps to create a **Mac Sonoma Virtual Machine (VMWare) in your Windows laptop** see this video: 

https://www.youtube.com/watch?v=h8oLSDUxDEw&t=857s

## 1. How to download/install VMWare WorkStation 17 Pro

We have to creat a new account in **Broadcom**

https://www.broadcom.com/

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/75269a1c-6543-4198-9226-9c9ee4470baa)

We have to follow this link to download the VMWare WorStation 17 Pro for personal use

https://support.broadcom.com/group/ecx/productdownloads?subfamily=VMware+Workstation+Pro

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/4443bd82-e817-4c90-9173-1e3c8c4adb06)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/4fc746b1-9f02-4b8b-9c2b-9e2d746578bb)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/1bab3ce2-cec3-4e6d-8cc4-10d3d8782497)

See the downloaded file

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/0d32376a-4f13-4adb-bec2-5b137b188856)

**Install VMWare WorkStation Pro 17 Administrator**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/5e0359fa-c0b5-470f-b14e-b18b49a6fc61)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/e6279d8a-b980-4af5-9a2c-26d83905f060)



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

## 4. Create/Configure Mac Sonoma Virtual Machine (with VMWare WorkStation Pro 17)

We create a new Virtual Machine(VM)

We first **open VMWare** 

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/f94271be-f8f1-4c8a-81ba-b8acd46dcbc5)

We click on **Create a New Virtual Machine** button 

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/1be9a4da-3266-444f-8e60-03590ddc295b)

We select the option we will select the operating system later and press the Next button

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/845a33d2-50c7-455c-bf4e-efcbf138a72f)

Then we select the Operating System **Mac OS**  and the **version 14**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/1bce6942-9c1b-4388-a178-b6d351e585d2)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/71eac6f0-0bce-4bdf-80c3-c09e4dd8c528)

We select the **VM name and location**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/389f2e65-a16a-41ff-882a-7537459bc57b)

We input the **VM hardrive space** 

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/7b6bd122-44a6-490e-b885-0c3c59c47d07)

Now we have to **customize the VM**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/b6c4a98c-a639-419d-816a-683d26a15627)

We configure the **VM Ram memory**. It is advisable to select **minimum 8 Gb**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/64f68232-274f-4334-a5fe-aacb10ec0dac)

We select the **number of processors and cores per processor**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/751c16a9-659e-4cbc-95ce-7fa37477f383)

We select the **Sonoma ISO immage file**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/ee50e558-c71a-40cd-a79b-67b7b2039262)

We choose the **network NAT adapter**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/594efd5b-d23d-4325-82aa-c46ac12280a4)

We set the **USB Controller**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/70766054-f07a-489e-bde4-66e93b5e1fc5)

We leave the default values for the **Sound Card*

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/7c58c24c-3b65-4e7b-92d6-b231b08aea69)

We finally input the **Display Settings**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/e3743b06-14c4-41a9-a248-de5b8cfe2712)

## 5. How to run the VM

We press on **Power on this virtual machine** button

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/b291a70c-840d-49c3-b899-f42e04462647)

Then we will be shown the following **Mac OS running window**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/60d8a64a-0478-48a1-a0ec-a5ab65589bdc)

We also will be asked to select the **Mac OS language (English)**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/9db3aeb5-3312-49f2-b6e6-2b1696a2d3b7)

We first select the **Disk Utility** and press the continue button

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/a0a4e811-702c-4493-a1a4-a660582df52d)

Now we have to **Erase VMWare Virtual SATA Hard Drive Media**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/6ff40d82-9bb4-4fc6-a232-a0797d0d436f)

We **input the hard drive name** and leave the other fields with the default values and press the Erase button

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/99383301-5274-4f26-97f1-00a421c2d17e)

To continue we press the **Done button**

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/1386ec3b-7e3f-47b0-8a59-64e9c5c21487)

We select the **Sonoma OS and press the continue** button

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/b804839f-e376-45a5-a4f8-ced51ad12264)

We select the **Country Region**(Spain)

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/42a459a7-83ec-476b-b0cb-1bd8d1af8be1)

We press continue in the Written and Spoken language screen

![image](https://github.com/luiscoco/macOS_Sonoma_VMWare/assets/32194879/26ae5ac8-0e16-47d6-8a5a-200ab92da6f5)


## 6. 



