# Overview

**procname** is a simple `LD_PRELOAD` library that sets the process name on Linux to the name specified in the environment variable `PROCNAME`.  This allows Java programs to show up in `top` or `ps acux` as their logical name rather than the generic `java`. It could also be useful for other language runtimes such as Python or Ruby.

# Usage

Run Java with the `LD_PRELOAD` and `PROCNAME` environment variables set:

    LD_PRELOAD=/path/to/libprocname.so PROCNAME=hello java -jar foo.jar
