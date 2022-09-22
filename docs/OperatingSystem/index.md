## 1、Linux 内核与 Windows 内核有什么区别

内核是操作系统中应用连接硬件设备的桥梁。至少具备以下四种基本能力：

* 管理进程、线程

* 管理内存

* 连接硬件设备

* 提供系统调用

操作系统分层：

```
flow
ap=>operation: Applications
ke=>operation: Kernel
cpu=>operation: CPU
me=>operation: Meory
de=>operation: Devices
ap->ke
ke->cpu
ke->me
ke->de
```
