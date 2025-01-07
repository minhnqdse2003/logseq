- ![Containers vs Virtual Machines: Key Differences and Benefits](https://k21academy.com/wp-content/uploads/2020/11/Docker-and-Vm-blog-image_result-1.webp){:height 446, :width 778}
- OS containing 2 layers: **Hardware** -> **OS Kernel** -> **Applications**
	- `OS Kernel`: man in the middle between Hardware and Applications to mange Cpu,Mem and Devices
- `Docker` & `VM` their both virtualization tools. But work at different layer of OS.
- ||Docker|VM|
  |Where |Virtualization of `Applications` Layer and use `Host kernel`|Virtualization of Applications and `boot` it own OS kernel|
  |Size|Docker image is much `smaller`|Could be couple of gigabyte large|
  |Speed|Docker container start and run faster|Slower due to boot their own OS Kernel and Application on top of it|
  |Compatibility|Can't run linux base docker image on the Windows kernel|VM of any OS can run on any OS Host|