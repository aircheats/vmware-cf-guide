# Patching the Windows Registry

Ok, now if we open our virtual machine and try to open crossfire we will get an error like this:

```
Sorry, this application cannot run under a Virtual Machine
```

In order to get rid of this error, you'll have to patch some entries in your Virtual Machines's Registry.  

!!! note
    Here you can find a [video demonstration](video) of how to apply the registry patch & watch its results.  

## Download Registry Patch

!!! info
    You can make your own registry patch but I'll leave you to download one totally free (it works perfectly).

This registry patch contains some required values which need to be changed in order to bypass security checks.  

**Download the <a href="https://up-to-down.net/61988/cfbypassregistry" target="_blank">reg-cf.reg</a>.**

!!! warning
    The link to download the reg patch is advertised. To support the work that has been done in creating this guide. Here you have a [video](tutorial_descargar) on how to download it in case you don't know. 

For people who **do not want** to skip advertising, I will leave you the code of the file so that you can create your own **.reg**. 
It is greatly appreciated that you download the file from the link!

```
  Windows Registry Editor Version 5.00

  [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Class\{4D36E968-E325-11CE-BFC1-08002BE10318}\0000]
  "DriverDesc"="Intel Graphics SVGA 3D"

  [HKEY_LOCAL_MACHINE\HARDWARE\DESCRIPTION\System\BIOS]
  "BaseBoardManufacturer"="Intel Corporation"
  "SystemManufacturer"="Asus, Inc."
  "SystemProductName"="Asus Platform"
```

## Use the Registry Patch

Now we will have to pass the registry file to the virtual machine.

Once you have the file on your Virtual Machine, simply **double-click** to execute it.  
You will see an information and get asked if you want to continue, press `Yes` to apply the registry patch.  

![](../../img/bypass-vm/4.png)

Once the changes applied successfully you're good to go.  

![](../../img/bypass-vm/5.png)

Now we can run Crossfire normally.

We already have a virtual machine bypassed.

In the next step we will learn how to use a bot so that the game does not detect the AFK
