![[FrozenSauce/Main/_Resources/FrozenSauce_Header.png]]
###### Alternatively, DInToss.DLL (Tossing out Dinput)

## Widescreen
- [ ] Fix Widescreen patch OR disable completely.
	- [ ] Prefer  Chimera/Vulpes widescreen patches if present.
	- [ ] Allow mouse cursor to access full screenspace instead of 4:3 rectangle.
## Rasterizer, Post-Processing
- [ ] Fix HUD scaling OR disable completely (Sniper scope? UI cache for sure)
	- [ ] Prefer Chimera HUD scaling
## UI Scale
- [ ] HUD scaling OR disable completely (Sniper scope? UI cache for sure)
	- [ ] Prefer Chimera HUD scaling
## FOV
- [ ] Correct FOV settings (Gearboxed FOV calculation. GB = subtract x pixels from resolution and multiply by (0.85?)
	- OpenSauce/Halo1/Halo1_CE/Game/CameraFov.inl
	- OpenSauce/Halo1/Halo1_CE/Memory/1.10/\_EngineLayout.Game.inl
	    - namespace fov
	- Prefer Chimera FOV settings
		- Keep FP Model View access?
## Overlay GUI
- [ ] Do not initialize any settings (e.g. motion blur) when menu/UI F7 is opened unless the setting could not be found in user settings file. Initialize setting to OFF!
- [ ] Checkbox to lock/unlock FOV slider to nearest multiple of 5
- [ ] Auto-configure button
- [ ] Allow old 3.0/3.1 FOV setting (mouse-movement transformation a la HAC2)
	- Because people love this novelty feature
## Engine Limit Extensions
- [ ] Increase view distance to known maximum value.
- [ ] Increase object view limit
	- [ ] Scale back based on performance?
- [ ] Limit Extensions
	- [ ] Increase particles?
	- [ ] Max Cache Size
- Upgrade Addresses: See `OpenSauce/Halo1/Halo1_CE/Memory/Pointers/HaloCE_110_Runtime_Manual.TagGroups`
## Bonus
- [ ] Look for areas where multi-tasking/multi-threading can be used.
- [ ] Look for areas where the post-processing pipeline can be optimized.
	- shrink buffers, convert textures to lesser colorspaces e.g. greyscale for height/depth maps.
- [ ] When Chimera is detected, attempt to pass Frozen Sauce settings to Chimera via Chimera's commands. For instance, checking HUD scaling checkbox for Open Sauce will instead pass "chimera_widescreen_fix 1" to the game command console and/or variants from different Chimera versions. Alternatively, pass the settings to Chimera's settings files (chimera.ini, chimera.bin, et cetera)
- [ ] Change tag extension method
	- [ ] Move non-vanilla tag definitions outside of vanilla tag definitions.