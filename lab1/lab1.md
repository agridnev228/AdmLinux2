1 продемонстрировать работу команд:
cat, ls, cp, mv, touch, rm, echo, cd,mkdir, rmdir,grep, less, pwd,diff, file, find, locate, head, tail, sort
```
alexey@ubuntu:/home$ cat file.txt
adadad
sadasd
sadasd
sadasdas
```
```
alexey@ubuntu:/home$ ls -la
total 28
drwxr-xr-x  6 root   root   4096 Oct 10 23:29 .
drwxr-xr-x 21 root   root   4096 Mar 17  2022 ..
drwxr-xr-x 23 alexey alexey 4096 Oct  8 00:27 alexey
-rw-r--r--  1 root   root     30 Oct 10 23:29 file.txt
drwxr-xr-x  2 root   root   4096 Mar 17  2022 softethervpn
drwxr-xr-x  4 root   root   4096 Mar 28  2022 v2ray
drwxr-xr-x  2 root   root   4096 Mar 24  2022 wiws
alexey@ubuntu:/home$ ls
alexey  file.txt  softethervpn  v2ray  wiws
```

alexey@ubuntu:/home$ sudo cp file.txt file2.txt
alexey@ubuntu:/home$ ls
alexey  file2.txt  file.txt  softethervpn  v2ray  wiws
alexey@ubuntu:/home$ cat file2.txt
adadad
sadasd
sadasd
sadasdas


alexey@ubuntu:/home$ sudo mv file2.txt file1.txt
alexey@ubuntu:/home$ ls
alexey  file1.txt  file.txt  softethervpn  v2ray  wiws

alexey@ubuntu:/home$ sudo rm file1.txt
alexey@ubuntu:/home$ ls
alexey  file.txt  softethervpn  v2ray  wiws

alexey@ubuntu:/home$ echo text
text

alexey@ubuntu:/home$ pwd
/home

alexey@ubuntu:/home$ sudo mkdir temp
alexey@ubuntu:/home$ ls
alexey  file.txt  softethervpn  temp  v2ray  wiws
alexey@ubuntu:/home$ sudo rmdir temp
alexey@ubuntu:/home$ ls
alexey  file.txt  softethervpn  v2ray  wiws


alexey@ubuntu:/home$ cat /etc/passwd| grep alexey
alexey:x:1000:1000:ubuntu,,,:/home/alexey:/bin/bash

alexey@ubuntu:/home$ less /var/log/syslog

Oct  7 22:56:37 ubuntu systemd[1]: rsyslog.service: Sent signal SIGHUP to main process 838 (rsyslogd) on client request.
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9253] policy: auto-activating connection 'netplan-ens33' (14f59568-5076-387a-aef6-10adfcca2e26)
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9377] device (ens33): Activation: starting connection 'netplan-ens33' (14f59568-5076-387a-aef6-10adfcca2e26)
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9443] device (ens33): state change: disconnected -> prepare (reason 'none', sys-iface-state: 'managed')
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9590] manager: NetworkManager state is now CONNECTING
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9654] device (ens33): state change: prepare -> config (reason 'none', sys-iface-state: 'managed')
Oct  7 22:56:37 ubuntu systemd[1]: logrotate.service: Deactivated successfully.
Oct  7 22:56:37 ubuntu systemd[1]: Finished Rotate log files.
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9970] device (ens33): state change: config -> ip-config (reason 'none', sys-iface-state: 'managed')
Oct  7 22:56:37 ubuntu NetworkManager[827]: <info>  [1665208597.9976] dhcp4 (ens33): activation: beginning transaction (timeout in 45 seconds)
Oct  7 22:56:38 ubuntu systemd[1028]: Queued start job for default target Main User Target.
Oct  7 22:56:38 ubuntu systemd[1028]: Created slice User Application Slice.
Oct  7 22:56:38 ubuntu systemd[1028]: Created slice User Background Tasks Slice.
Oct  7 22:56:38 ubuntu systemd[1028]: Created slice User Core Session Slice.
Oct  7 22:56:38 ubuntu systemd[1028]: Started Pending report trigger for Ubuntu Report.
Oct  7 22:56:38 ubuntu systemd[1028]: Reached target Paths.
Oct  7 22:56:38 ubuntu systemd[1028]: Reached target Timers.
Oct  7 22:56:38 ubuntu systemd[1028]: Starting D-Bus User Message Bus Socket...
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on GnuPG network certificate management daemon.
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on GnuPG cryptographic agent and passphrase cache (access for web browsers).
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on GnuPG cryptographic agent and passphrase cache (restricted).
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on GnuPG cryptographic agent (ssh-agent emulation).
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on GnuPG cryptographic agent and passphrase cache.
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on PipeWire Multimedia System Socket.
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on debconf communication socket.
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on Sound System.
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on REST API socket for snapd user session agent.
Oct  7 22:56:38 ubuntu systemd[1028]: Listening on D-Bus User Message Bus Socket.
Oct  7 22:56:38 ubuntu systemd[1028]: Reached target Sockets.
Oct  7 22:56:38 ubuntu systemd[1028]: Reached target Basic System.
Oct  7 22:56:38 ubuntu systemd[1]: Started User Manager for UID 125.
Oct  7 22:56:38 ubuntu systemd[1]: Started Session c1 of User gdm.
Oct  7 22:56:38 ubuntu systemd[1028]: Started PipeWire Multimedia Service.
Oct  7 22:56:38 ubuntu systemd[1028]: Started PipeWire Media Session Manager.
Oct  7 22:56:38 ubuntu systemd[1028]: Starting Sound Service...
Oct  7 22:56:38 ubuntu systemd[1028]: Starting Tracker metadata extractor...
Oct  7 22:56:38 ubuntu systemd[1028]: Started D-Bus User Message Bus.
Oct  7 22:56:38 ubuntu dbus-daemon[826]: [system] Activating via systemd: service name='org.freedesktop.RealtimeKit1' unit='rtkit-daemon.service' requested by ':1.26' (uid=125 pid=1068 comm="/usr/bin/pipewire-media-session " label="unconfined")
Oct  7 22:56:38 ubuntu systemd[1]: Starting RealtimeKit Scheduling Policy Service...
Oct  7 22:56:38 ubuntu dbus-daemon[1096]: [session uid=125 pid=1096] AppArmor D-Bus mediation is enabled
Oct  7 22:56:38 ubuntu dbus-daemon[826]: [system] Successfully activated service 'org.freedesktop.RealtimeKit1'
Oct  7 22:56:38 ubuntu systemd[1]: Started RealtimeKit Scheduling Policy Service.
Oct  7 22:56:38 ubuntu rtkit-daemon[1105]: Successfully called chroot.
Oct  7 22:56:38 ubuntu rtkit-daemon[1105]: Successfully dropped privileges.
Oct  7 22:56:38 ubuntu rtkit-daemon[1105]: Successfully limited resources.

alexey@ubuntu:/home$ find wiws
wiws
wiws/docker-compose.yaml



alexey@ubuntu:/home$ tail -f /var/log/syslog
Oct 11 00:53:45 ubuntu systemd[1]: Starting Network Manager Script Dispatcher Service...
Oct 11 00:53:45 ubuntu dbus-daemon[825]: [system] Successfully activated service 'org.freedesktop.nm_dispatcher'
Oct 11 00:53:45 ubuntu systemd[1]: Started Network Manager Script Dispatcher Service.
Oct 11 00:53:47 ubuntu NetworkManager[827]: <info>  [1665474827.2798] manager: NetworkManager state is now CONNECTED_GLOBAL
Oct 11 00:53:57 ubuntu systemd[1]: NetworkManager-dispatcher.service: Deactivated successfully.
Oct 11 00:55:01 ubuntu CRON[9338]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
Oct 11 01:05:02 ubuntu CRON[9366]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
Oct 11 01:11:51 ubuntu kernel: [12670.356320] perf: interrupt took too long (4554 > 4121), lowering kernel.perf_event_max_sample_rate to 43750
Oct 11 01:15:01 ubuntu CRON[9396]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
Oct 11 01:17:01 ubuntu CRON[9408]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)


alexey@ubuntu:/home$ ls -l|sort -k9
total 20
drwxr-xr-x 23 alexey alexey 4096 Oct  8 00:27 alexey
-rw-r--r--  1 root   root     30 Oct 10 23:29 file.txt
drwxr-xr-x  2 root   root   4096 Mar 17  2022 softethervpn
drwxr-xr-x  4 root   root   4096 Mar 28  2022 v2ray
drwxr-xr-x  2 root   root   4096 Mar 24  2022 wiws

alexey@ubuntu:/home$ diff file.txt file2.txt
5,6d4
< asdadsa
< 

alexey@ubuntu:/home$ file file.txt
file.txt: ASCII text

alexey@ubuntu:/home$ locate file.txt
/home/file.txt
/usr/lib/python3/dist-packages/pbr/tests/testpackage/extra-file.txt
/usr/lib/python3/dist-packages/pbr/tests/testpackage/git-extra-file.txt
/usr/share/doc/alsa-base/driver/Procfile.txt.gz

2 показать содержимое path, добавить в path дополнительный путь

alexey@ubuntu:/home$ echo $PATH
/home/alexey/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
alexey@ubuntu:/home$ export PATH=$PATH:/home/alexey
alexey@ubuntu:/home$ echo $PATH
/home/alexey/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin:/home/alexey


3 продемонстрировать перенаправление вывода в файл
  root@ubuntu:/home# echo "text" > file.txt
root@ubuntu:/home# ls
alexey  file2.txt  file.txt  softethervpn  v2ray  wiws
root@ubuntu:/home# cat file.txt
text

      
4 вызвать команду с ошибкой и перенаправить вывод ошибки в файл

ls -lz 2> error.txt

5 перенаправить стандартный ввод в программу

cat < error.txt
ls: invalid option -- 'z'
Try 'ls --help' for more information.

6 создать архив, распаковать архив

tar -cf archive.tar temp/
tar -xvf archive.tar
