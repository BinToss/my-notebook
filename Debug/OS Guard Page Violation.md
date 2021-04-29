```
(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
*** WARNING: Unable to verify checksum for J:\Games\SPV3\SPV3.3\mods\dinput8.dll
eax=00000001 ebx=0019ceed ecx=7af2806c edx=1820ba52 esi=1820ba52 edi=0019d03c
eip=7aee2562 esp=0019ced0 ebp=0019cff0 iopl=0         nv up ei pl nz na po nc
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010202
dinput8!DirectInput8Create+0x1e102:
7aee2562 8a02            mov     al,byte ptr [edx]          ds:002b:1820ba52=00
```

>> Open Sauce violates yet another address...
>> Unable to verify checksum: This is because OS replaces DirectInput. Let's not do that, shall we?
