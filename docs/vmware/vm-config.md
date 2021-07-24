# Updating Virtual Machine Configuration

In order to run the Crossfire game in a virtual machine we have to modify the virtual machine configuration.

!!! info
    If you want to copy CrossFire from your Host System make sure to do this before adjusting the configuration.  
    It seems like adjusting the configuration will break drag-and-drop feature.

![](../../img/bypass-vm/1.png)

We close the virtual machine and right click on it and open its directory.

![](../../img/bypass-vm/2.png)

In the following folder we will have to locate a file with the extension .vmx and open it with any text editor.

!!! tip
    I recommend using Notepadd ++ or Visual Studio Code

Now in the .vmx file we have to add the following lines at the end:

```
monitor_control.restrict_backdoor = "true"
isolation.tools.getPtrLocation.disable = "true"
isolation.tools.setPtrLocation.disable = "true"
isolation.tools.setVersion.disable = "true"
isolation.tools.getVersion.disable = "true"
monitor_control.disable_directexec = "true"
monitor_control.disable_btmemspace = "true"
```

!!! info
    Credits and special thanks to 0vis (Discord: 0vis#1008) for providing the proper configuration properties above.

![](../../img/bypass-vm/3.png)

Save the file and close it.  
You can now power it up again and proceed with the registry patch.  
