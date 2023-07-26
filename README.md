# YDLidarGS2

sdk(YDLidar GS2) : https://github.com/YDLIDAR/EaiSdkForGS2/blob/master/samples/main.cpp

sdk(YDLidar) : https://github.com/YDLIDAR/YDLidar-SDK/blob/master/doc/YDLIDAR_SDK_API_for_Developers.md



c/cpp file
```
unix_timer.cpp 0
unix_serial.cpp 0
serial.c 0 
ydlidar_driver.cpp 0
list_ports_linux.cpp 0
CYdLidar.cpp 0
new_test_lidar_copy.c 0
```

include
```
timer.h 0
unix_serial.h 0
serial.h 0
common.h 0
unix.h 0
ydlidar_driver.h 0
CYdLidar.h 0
unix_serial.h 0
timer.h 0 
v8stdint.h 0
angles.h 0
utils.h 0
locker.h 0
thread.h 0
ydlidar_protocol.h 0
help_info.h 0
```

complie
```
aarch64-linux-gnu-g++ -o test_arm64 CYdLidar.cpp unix_timer.cpp unix_serial.cpp serial.c ydlidar_driver.cpp list_ports_linux.cpp new_test_lidar_copy.c -lpthread -static
```


files struct
```
unix_timer.cpp
  -> #include "timer.h"
     ...

unix_serial.cpp
  #include <stdio.h>
  #include <string.h>
  #include <sstream>
  #include <unistd.h>
  #include <fcntl.h>
  #include <sys/ioctl.h>
  #include <sys/signal.h>
  #include <sysexits.h>
  #include <errno.h>
  #include <paths.h>
  #include <sys/param.h>
  #include <pthread.h>
  #include <poll.h>
  #include <sys/utsname.h>
  #include <asm/ioctls.h>
  #include <linux/serial.h>
  #include <sys/select.h>
  #include <sys/time.h>
  #include <sys/stat.h>
  #include <time.h>
  -> #include "unix_serial.h"
     ...

serial.c
  -> #include "serial.h"
     ...
  -> #include "common.h"
     ...

ydlidar_driver.cpp
  -> #include "ydlidar_driver.h"
     ...
  -> #include "common.h"
     ...
  #include <math.h>

list_ports_linux.cpp
  #include <vector>
  #include <string>
  #include <sstream>
  #include <stdexcept>
  #include <iostream>
  #include <fstream>
  #include <cstdio>
  #include <cstdarg>
  #include <cstdlib>
  #include <glob.h>
  #include <sys/types.h>
  #include <sys/stat.h>
  #include <unistd.h>
  -> #include "serial.h"
     ...

CYdLidar.cpp
  -> #include "CYdLidar.h"
  -> #include "common.h"
      --> #include "unix.h"
            #include <stdio.h>
            #include <stdint.h>
            #include <string.h>
            #include <stdlib.h>
            #include <assert.h>
            #include <math.h>
            #include <time.h>
            #include <stdarg.h>
            #include <iostream>
            #include <string>
            #include <unistd.h>
            #include <errno.h>
            #include <pthread.h>
            #include <sys/time.h>
            #include <sys/types.h>
            #include <sys/stat.h>
            #include <fcntl.h>
            #include <sys/ioctl.h>
            #include <sys/select.h>
            #include <time.h>
      --> #include "unix_serial.h"
            #include <pthread.h>
            #include <assert.h>
            #include <termios.h>
            ---> #include "serial.h"
                 ...
      --> #include "locker.h"
          ...
      --> #include "thread.h"
          ...
      --> #include "timer.h"
            ---> #include "v8stdint.h"
            #include <assert.h>
            #include <time.h>
            #include <inttypes.h>
  #include <map>
  -> #include "angles.h"
  #include <numeric>

new_test_lidar_copy.c
  -> #include "CYdLidar.h"
    --> #include "utils.h"
    --> #include "ydlidar_driver.h"
        #include <stdlib.h>
          #include <atomic>
          #include <map>
          ---> #include "serial.h"
                  #include <limits>
                  #include <vector>
                  #include <string>
                  #include <cstring>
                  #include <sstream>
                  ----> #include "v8stdint.h"
                          #include <stddef.h>
                          #include <stdio.h>
                          #include <stdlib.h>
                          #include <string>
                          #include <string.h>
                          #include <signal.h>
                          #include <cerrno>
                          #include <stdexcept>
                          #include <csignal>
                          #include <sys/stat.h>
          ---> #include "locker.h"
                  #include <assert.h>
                  #include <pthread.h>
                  #include <sys/time.h>
                  #include <sys/types.h>
                  #include <sys/stat.h>
                  #include <errno.h>
          ---> #include "thread.h"
                  ----> #include "v8stdint.h"
                  #include <pthread.h>
                  #include <assert.h>
          ---> #include "ydlidar_protocol.h"
                  ----> #include "v8stdint.h"
                  #include <vector>
          ---> #include "help_info.h"
                  ----> #include "ydlidar_protocol.h"
                  #include <map>
    #include <math.h>
  #include <iostream>
  #include <string>
  #include <algorithm>
  #include <cctype>
```

