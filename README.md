# Dell-7070-mff-hackintosh  
Dell-7070-mff黑苹果OpenCore引导 所有硬件均工作 iMessage自行添加 网卡更换DW1560  
  
硬件  
处理器：Intel Core i5-9500t  
芯片组：Intel Q370  
内存：32G DDR4 2666 三星  
显卡：UHD630  
声卡：ALC255(内置扬声器+耳麦一体+音频输出)  
网卡：Intel I219-LM7  
无线网卡：DW1560(BCM94352z)  
硬盘1：HP EX920 1TB Nvme固态  
硬盘2：英睿达MX500 1TB SSD固态  
  
正常工作：  
1.变频 HWP  
2.显卡、网卡、声卡、无线网卡、蓝牙  
3.USB已定制  
4.睡眠(电源键菜单+电源键唤醒+键盘唤醒+鼠标唤醒+蓝牙唤醒+网卡唤醒)  
  
不正常工作：  
1.无  
  
目前运行在10.15.3环境中 状态良好 后续会持续跟进引导的更新  


## BIOS Settings
* General → Advanced Boot Options: ***uncheck***
* System Configuration → SATA Operation: ***AHCI***
* Secure Boot → Secure Boot Enable: ***Disabled***
* Intel® Software Guard Extensions™ → Intel® SGX™ Enable: ***Disabled***
* Power Management → Block Sleep: ***check***
* Virtualization Support → VT for Direct I/O: ***uncheck***

## BIOS Settings via GRUB (Optional)
* Set Pre-Allocated DVMT to 64M: 
***setup_var 0x8DC 0x02***
* Disable CFG lock: 
***setup_var 0x5BE 0x00***


更新(2020-09-02):  
1.11.xBeta 新增支持11.x测试版 目前测试通过11.0 Beta版(20A5354i)  注意 该目录下引导并不支持10.15.x(暂时没精力去修正 好久没关注OC发展了 脱节)  

更新(2020-11-22):  
1.目前测试通过11.0.1正式版(20B29)  10.15.x(测试通过 感谢@openaphid)  

更新(2020-11-25):  
1.新增对应Intel 9560网卡配置 自行测试

更新(2021-01-08):  
1.更新OpenCore和Kexts， 增加Intel无线网卡支持，目前测试11.1正式版(20C69)通过  
