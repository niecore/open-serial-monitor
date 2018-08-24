# open-serial-monitor (in dev)

A software for windows that makes serial port monitoring easy.

**Table of contents**

1. Goals
2. Related projects
3. Documentation
4. Contribution

## Goals

This software should give developers the chance to monitor/observe/log/watch serial ports that are used by other applications.

1.  Create an command line application that takes the serial port identification of an existing port that should be monitored.
    This command will print all serial traffic of this port to `stdout`.
    
    The parameter `--direction` should allow the user to either monitor `incoming`, `outgoing` or traffic in `both` directions.
    
    The parameter `--driver_operations` should allow the user monitor driver operations like `PORT_OPEN`, `PORT_CLOSED` or `...` as well.
    
2.  Create an command line application that creates an virtual serial port which can be opened by any other other application.
    All traffic that is send to this serial port should be forwarded to `stdout`. All traffic that is send to `stdin` should be transfered to the application which has opened this virtual serial port.  

3.  Create an command line application that connects an existing serial port (see 1.) with an virtual serial port (see 2.).
    All traffic that is received on the real serial port should be forwarded to the virtual serial port. All traffic that is send to the virtual serial port should be forwarded to the real serial port.
    All driver operation must be fotwarded as well. The forwarded traffic (in both directions) should be displayed in `stdout`.

## Backlog

1. Provide multi platform support
2. Store and recall serial port environments from configuration files
3. Provide graphical user interface

## Related projects

1.  com0com

## Documentation

to be continued

## Contribution

to be continued