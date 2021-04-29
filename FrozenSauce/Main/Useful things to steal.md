- Move gamestate modifications out of the main stack
	- https://github.com/Sigmmma/Vulpes/pull/69
- Set memory address protection/permission to original state after modification
	- Chimera did this a long time ago. Need reference/source.
- Map and resource compression
	- https://github.com/SnowyMouse/invader/issues/125#issuecomment-597841772
- Move tag class/struct modifications to new classes/structs. Don't dirty up the vanilla classes/structs.
	- Invader-build
- Signature Scanning
	- https://github.com/SnowyMouse/chimera/commit/e5729d9390fe0bb8e24981a113cc2e36bab3be0e
- Modernize swapchain and device creation
	- https://github.com/PCSX2/pcsx2/commit/210336d8c17925e11ac15e849b0d3336a17a876e

https://github.com/SnowyMouse/invader/issues/171
Rename classes/definitions with "namespace" nomenclature.
E.g. "extended_bitmaps" -> "opensauce_yelo_bitmaps

![[FrozenSauce/Main/_Resources/Vulpes_IMGUI.png]]