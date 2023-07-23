# Basic-_linux_commands   

##  Linux Operating system  | Debian  Distribution of linux | using zsh shell

### List of debian distros
* Ubuntu
* Linux Mint
* MX linux
* Parrot os
* Kali linux

<hr>

Basic linux commands used on regular basis  <br>



<hr>

### Check which type of shell is using 
  <blockquote>
  $ echo $0     [this commands shows the which type of shell you are using.]
 </blockquote>


### Switch  user to root user
 <blockquote>
   $ sudo su     [imp: sudo su  full form is Super  User Do]
 </blockquote>
 
 ### Switch  root user to user
 <blockquote>
   $ sudo su   username
 </blockquote>

 ### switching the folders
 <blockquote>
   $ cd directory-name [imp: cd full form is change directory.]
 </blockquote>
 
 
  ### checking the current working directory
 <blockquote>
   $ pwd [output: /home/Downloads]
 </blockquote>
 
 
 
 ### listing the items of particular folder 
 <blockquote>
   $ ls            [imp: ls command is used for listing the particular items of the directory] <br>
   $ ls -ltr       [imp: this command shows the recent file or folder to the bottom of the list. it helps in easily finding the file or folder] 
 </blockquote>
 
 
 ### making the directory
 <blockquote>
   $ mkdir directory-name> 
 </blockquote>
 
### removing directory
 <blockquote>
   $ rm -r directory-name
 </blockquote>
 
 
 
 
 
 ### creating the file
 <blockquote>
   $ touch file-name
 </blockquote>
 
 ### removing the file
 <blockquote>
   $ rm -f file-name
 </blockquote>
 
 
 ### reading the content of the file
 <blockquote>
   $ cat file-name
 </blockquote>
 
 
 ### copy and paste commands in terminal
 <blockquote>
    For copy select using mouse and than ctrl+shift+c  <br>
    For paste  ctrl+shift+v
 </blockquote>

### cpu/processor information
 <blockquote>
   $ cat proc/cpuinfo   [imp: it will gives you info about processsor,cpu family, model,vendorid,cpu Mhz,cache size,many more]
 </blockquote>
 
 
 
  ### Checking ther services which are  running 
 <blockquote>
    $ service --status-all     [this command list all the services that are currently running]
 </blockquote>
 
 
 
 <hr>
 
 ### Linux boot time  detail :- Taking too much time on booting 
   
  <blockquote>
    
       $ systemd-analyze
      
         Result:-  Startup finished in 7.003s (firmware) + 6.682s (loader) + 15.391s (kernel) + 1min 14.216s
         (userspace) = 1min 43.294s  graphical.target reached after 1min 13.328s in userspace

  </blockquote>
  <hr>
 
 ### Checking which service is taking too much time in booting
 <blockquote>
  
 $ systemd-analyze blame <br>
  
 result:- 
 45.817s plymouth-quit-wait.service  <br>
34.718s docker.service <br>
10.450s networking.service <br>
10.411s systemd-journal-flush.service  <br>
 8.872s NetworkManager-wait-online.service <br>
 8.199s accounts-daemon.service <br>
 6.312s polkit.service <br>
 6.050s NetworkManager.service  <br>
 6.006s phpsessionclean.service  <br>
 5.913s systemd-logind.service  <br>
 5.708s dev-sda2.device  <br>
 4.953s udisks2.service  <br>
 3.357s fwupd.service  <br>
 2.626s mono-xsp4.service  <br>
 2.622s smartmontools.service  <br>
 2.199s systemd-udevd.service  <br>
 2.023s systemd-modules-load.service  <br>
 1.904s rsyslog.service  <br>
 1.586s packagekit.service  <br>
 1.419s e2scrub_reap.service  <br>
 1.229s plymouth-start.service  <br>
 1.124s ModemManager.service  <br>
  986ms systemd-tmpfiles-setup-dev.service  <br>
  899ms systemd-fsck@dev-disk-by\x2duuid-000D\x2d8E28.service  <br>
  898ms systemd-udev-trigger.service  <br>
  697ms systemd-sysusers.service  <br>
  647ms keyboard-setup.service  <br>
  589ms systemd-tmpfiles-setup.service  <br>
  504ms run-rpc_pipefs.mount
  501ms gdm.service
  455ms wpa_supplicant.service
  414ms colord.service
  402ms binfmt-support.service
  391ms systemd-journald.service
  364ms user@1000.service
  360ms boot-efi.mount
  348ms systemd-random-seed.service
  300ms modprobe@fuse.service
  273ms dev-disk-by\x2duuid-c5bb098e\x2da669\x2d4589\x2db8ec\x2d33d555bc16c0.swap
  241ms systemd-sysctl.service
  241ms upower.service
  219ms ifupdown-pre.service
  202ms modprobe@configfs.service
  196ms systemd-rfkill.service
  159ms systemd-remount-fs.service
  118ms nfs-config.service
  114ms proc-sys-fs-binfmt_misc.mount
   99ms dev-hugepages.mount
   98ms dev-mqueue.mount
   96ms sys-kernel-debug.mount
   95ms sys-kernel-tracing.mount
   90ms systemd-update-utmp.service
   32ms systemd-user-sessions.service
   27ms console-setup.service
   22ms rtkit-daemon.service
   16ms kmod-static-nodes.service
   11ms plymouth-read-write.service
    9ms modprobe@drm.service
    8ms user-runtime-dir@1000.service
    7ms systemd-update-utmp-runlevel.service
    3ms sys-fs-fuse-connections.mount
    2ms sys-kernel-config.mount
  986us docker.socket

 </blockquote>

 
 
 ### stopping the docker service taking too much time on booting
  
   <blockquote>
   first Chekct the status <br>
   $ systemctl status docker  <br>
   $  sudo systemctl stop docker     [ it will stop the docker service running on but incase  it gives :- Warning: Stopping docker.service, but it can still be activated by:   docker.socket ]  than you have to run this command <br>
      
   $ sudo systemctl stop docker.socket
 
   </blockquote>
  
  
   ### Commands realtaed to mysql 
  
   <blockquote>
    Check mysql service status <b>
  
    $ sudo service mysql status
  
  <b>
   
   
    start: - 
    $ sudo service mysql start

     Stop :- 
    $ sudo service mysql stop
 
   </blockquote>
  
 
 

 ### command to kill any running port on tcp
   sudo fuser -k 8080/tcp
 

