# Fly and move Phenox2(autonomous)

##Movie of flight
[![Alt text for your video](http://img.youtube.com/vi/fEEkiQL5E1I/0.jpg)](http://www.youtube.com/watch?v=fEEkiQL5E1I)


This tutorial explains following works using Ubuntu14.04 as host-PC.

1. Startup Phenox2 from battery, connect to host-PC using ssh.  
2. Check self state (px_selfstate).
3. Prepare flight space checking number of visual feature points from bottom camera.
4. Put Phenox2 on the ground, and blow whisle to start hovering autonomously.
5. Move Phenox2 to forward keeping same height.

Also, please take care of following points.

 - Prepare wide and planer space(3m x 3m at least) and heigh(2.5m at least) without any object on the ground.  
 - Try experiment in indoor environment, and turn off air conditioner.  
 - Remember that flying Phenox2 can be stopped immediately by holding one of legs and tilt it largely.  
 - In this tutorial, Phenox2 move forward about 1.5m, so prepare enough space in front side of Phenox2.
  
# 1. Setup supply power and communication
First, please check that 4 corners of main board are fixed to silicon ring correctly. Please setup supply power using battery as described in [Power supply](../start/power.md), and setup communication using ssh as described in [Communication](../start/com.md).
 
# 2. Create project
Copy tutorial to make custom projects as follows..

```bash
phenox# cd /root/phenox/work/
phenox# cp -a tutorial_move myproject_move
```
# 3. Build project
Build  myproject_move as default setting.
```bash
phenox# cd /root/phenox/work/myproject_move
phenox# make clean all
```
Now, executable file "main" is created.

# 4. Execute program
The sequence of this tutorial program are as follows.

1. Initialize CPU1(flight control system) for 3 seconds.
2. Wait for whisle sound printing selfstate. 
3. Start hovering when whisle sound is detected.
4. Hovers to keep same position for about 8 seconds, then go forward about 1.5m.
5. Users grub one of legs of Phenox2 and tilt it largely to stop Phenox2.

Before running program, please put Phenox2 on the ground and do not move it until message "CPU0:Finished Initialization" appears. If users move Phenox2 during initialization, CPU1 detects movement and stops initialization. When this happens, please reboot Phenox2 by "reboot" command.

Now, let's start "main".
```bash
phenox# ./main
```

After initialization, members of selfstate (`degx`, `degy`, `degz`, `vision_tx`, `vision_ty`, `vision_tz`, `height`) and number of feature points are printed in terminal.

# 5. Prepare flight environment (needed only first time of flight)
Please hold Phenox2 and move above flight space to check number of feature points, and put markers on the ground if needed. 15 feature points are enough to estimate self position stably.

# 6. Fly Phenox2
After flight space is prepared, put Phenox2 on the ground, and blow whisle near Phenox2 strongly. Phenox2 operates 3 seconds of start up of motors, and takes off (`PX_UP`). Then, Phenox2 enters hover state (`PX_HOVER`) and try to fly at same position for about 8 seconds. Then, Phenox2 moves forward about 1.5m, and try to keep the same position. 

# 7. Stop Phenox2
Flying Phenox2 can be stopped immediately by holding one of legs and tilt it largely.

To shutdown Phenox2, type following command.
```bash
phenox# halt
```
