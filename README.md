# DebugIt module

The DebugIt module is used by lots of the RISC OS source to provide a
really simple way of writing out debug to another part of the system.
Essentially, you can have lots of different DebugIt modules that write
to different places.

The interface for DebugIt is simple - the first SWI of the module
is the equivalent of OS_WriteC, takes a character in R0. The characters
may include CR, LF (or LF, CR) sequences.

This implementation writes to the SysLog module using the log name
`DebugIt`. As can be seen the code is very simple, so feel free to write
some other implementation if necessary.


