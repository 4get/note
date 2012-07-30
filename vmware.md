
= win7脚本启动vmware虚拟机 =
"C:\Program Files (x86)\VMware\VMware VIX\vmrun.exe" start "ubuntu-10.04.4-desktop-amd64.vmx" nogui


= ubuntu虚拟机文件移动以后，网络不通 =
rm /etc/udev/rules.d/70-persistent-net.rules 
