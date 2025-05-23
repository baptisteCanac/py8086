# Py8086

This is a _very_ downstripped 8086 emulator.
It has an interactive debugger and a disassembler.

License: Creative commons, see:
http://creativecommons.org/licenses/by-sa/3.0/

Would be happy to hear if you do something fun with it :)
julien dot aubert at gmail dot com

Note: the program "codegolf" was not made by me, it was made by "copy"
http://codegolf.stackexchange.com/users/3428/copy
See here: http://codegolf.stackexchange.com/questions/4732/emulate-an-intel-8086-cpu

=== HOW-TO ===

Run (requires curses):

    python emu8086.py

Interactive debugger:
    
    python dbg.py

Output all states:
    
    python dbg.py a

=== TEST ===

Run unit tests:
    
    python emu8086_test.py

Run texttest:
    1    enter directory "texttest"
    2    start texttest (tested on version 3.22)
    3    in the left window under "texttest (e86)" select "RunProgram" (or "Disasm" to test the disasm output)
    4    press Run

This test runs the output of all states and compares the output with a known correct output.
This is a good integration test to make sure changes do not break the behavior.
For more info about texttest see: http://texttest.carmen.se/index.php?page=download

=== MORE INFO ===

It only supports the bare minimum required to run a program "codegolf".
See here: http://codegolf.stackexchange.com/questions/4732/emulate-an-intel-8086-cpu

Not supported:
    segments
    prefixes
    interrupts or port IO
    string functions
    two-byte opcodes 
    floating point   

Instructions supported:
    mov, push, pop, xchg
    add, adc, sub, sbb, cmp, and, or, xor
    inc, dec
    call, ret, jmp
    jb, jz, jbe, js, jnb, jnz, jnbe, jns
    stc, clc
    hlt, nop

Flags supported:
    carry, zero and sign flags

