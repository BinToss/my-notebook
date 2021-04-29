Caused by OS, dgVoodoo, or ReShade. Likely ReShade.

Guard Page Violations
d3dx9_43!D3DXTex::CImage::SaveJPG
```
0:000> g

(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
eax=00000000 ebx=00000000 ecx=5fe214bc edx=40000060 esi=18938000 edi=0019c83c
eip=5fef8d72 esp=0019c428 ebp=0019c6b0 iopl=0         nv up ei pl zr na pe nc
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010246
d3dx9_43!D3DXTex::CImage::SaveJPG+0x193:
5fef8d72 8b1486          mov     edx,dword ptr [esi+eax*4] ds:002b:18938000=00000000

0:000> g

(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
eax=00000400 ebx=00000c00 ecx=00000000 edx=00000000 esi=18938000 edi=0019c83c
eip=5fef8d72 esp=0019c428 ebp=0019c6b0 iopl=0         nv up ei ng nz na po cy
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010283
d3dx9_43!D3DXTex::CImage::SaveJPG+0x193:
5fef8d72 8b1486          mov     edx,dword ptr [esi+eax*4] ds:002b:18939000=00000000

0:000> gh

(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
eax=00000080 ebx=00000180 ecx=00000000 edx=00000000 esi=18939e00 edi=0019c83c
eip=5fef8d72 esp=0019c428 ebp=0019c6b0 iopl=0         nv up ei ng nz na pe cy
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010287
d3dx9_43!D3DXTex::CImage::SaveJPG+0x193:
5fef8d72 8b1486          mov     edx,dword ptr [esi+eax*4] ds:002b:1893a000=00000000

0:000> gh

(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
eax=00000480 ebx=00000d80 ecx=00000000 edx=00000000 esi=18939e00 edi=0019c83c
eip=5fef8d72 esp=0019c428 ebp=0019c6b0 iopl=0         nv up ei ng nz na pe cy
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010287
d3dx9_43!D3DXTex::CImage::SaveJPG+0x193:
5fef8d72 8b1486          mov     edx,dword ptr [esi+eax*4] ds:002b:1893b000=00000000

0:000> gh

(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
eax=00000100 ebx=00000300 ecx=00000000 edx=00000000 esi=1893bc00 edi=0019c83c
eip=5fef8d72 esp=0019c428 ebp=0019c6b0 iopl=0         nv up ei ng nz na po cy
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010283
d3dx9_43!D3DXTex::CImage::SaveJPG+0x193:
5fef8d72 8b1486          mov     edx,dword ptr [esi+eax*4] ds:002b:1893c000=00000000

0:000> gh

(5674.1f60): Guard page violation - code 80000001 (first chance)
First chance exceptions are reported before any exception handling.
This exception may be expected and handled.
eax=00000500 ebx=00000f00 ecx=00000000 edx=00000000 esi=1893bc00 edi=0019c83c
eip=5fef8d72 esp=0019c428 ebp=0019c6b0 iopl=0         nv up ei ng nz na po cy
cs=0023  ss=002b  ds=002b  es=002b  fs=0053  gs=002b             efl=00010283
d3dx9_43!D3DXTex::CImage::SaveJPG+0x193:
5fef8d72 8b1486          mov     edx,dword ptr [esi+eax*4] ds:002b:1893d000=00000000
```