#This is a config for high cuncurrency system.

##Background:
When I am working on a push system(with up to 300 million TCP connections per server), the system configuration bugged a lot. So I thought this might
help others if some of you running into the same problem.

##First of all:
Make sure your server has enough memory. And then change the server ulimit parameters to :
```
core file size          (blocks, -c) 0
data seg size           (kbytes, -d) unlimited
scheduling priority             (-e) 0
file size               (blocks, -f) unlimited
pending signals                 (-i) 1030528
max locked memory       (kbytes, -l) 64
max memory size         (kbytes, -m) unlimited
open files                      (-n) 8000000
pipe size            (512 bytes, -p) 8
POSIX message queues     (bytes, -q) 819200
real-time priority              (-r) 0
stack size              (kbytes, -s) 8192
cpu time               (seconds, -t) unlimited
max user processes              (-u) 1030528
virtual memory          (kbytes, -v) unlimited
file locks                      (-x) unlimited
```

Then check out the sysctl.conf file.
