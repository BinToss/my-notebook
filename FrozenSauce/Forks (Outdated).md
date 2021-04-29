Refer to https://github.com/yumiris/opensauce/ for known forks

### OSv5
- Adds GameSpyOpen as a shared include.  Already in OS4?
	- Why? Specifically for ED?
	- Also added lzma/lzwa/7zip as a shared include
	- Commits:
		- B849642c [Corpen] Added GameSpyOpen
		- 1a4fbb61 [Corpen] Added 7zip
		- 5565d84d [Corpen] Numerous fixes (to GameSpy Core)
		- 6eb2aa6b [Bipolar Aurora] Add Gamespy SDK bug fix
		- 223b1e2b [Bipolar Aurora] Delete the bug fix
		- 3fa07dc5 [Bipolar Aurora] Re-add the bug fix to the correct directory 
 
### Sprinkles' Code Cleanup
Only has changes to Halo 1 BlamLib
- [4d1d1ab3] Adds some info about Weapon structure.
	- `OpenSauce\shared\Include\blamlib\Halo1`
		- Items
			- weapon_structures.hpp
		- objects
			- objects_structures.hpp
	- Will this break any references?

### HM OS
https://github.com/HaloMods/OpenSauce/
imported to Yumiris/OpenSauce
