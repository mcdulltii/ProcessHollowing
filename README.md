# Process Hollowing

## Building

```
> cmake .
```

To show(1)/hide(2) console window when running executable:

```
- Properties
  - Linker
    - System
      - SubSystem: 
	    1. Console (/SUBSYSTEM:CONSOLE)
		2. Windows (/SUBSYSTEM:WINDOWS)
    - Advanced
      - Entry Point
	    1. (BLANK)
		2. mainCRTStartup
```

Default: hidden

## Reference

- https://github.com/hasherezade/demos/tree/master/run_pe
