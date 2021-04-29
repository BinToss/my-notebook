Beware: This document was originally a very messy note in OneNote with images thrown in arbitrary locations.

## Note 0
RE: Third party dependencies...
F it. Source code is scrapped in favor of libraries.
	- At the time this was written, OpenSauce compiled against the Headers of its dependencies instead of pre-compiled binaries.

## Note 1
`branch:cleanup-final`
Boost path: `"../external_ _libraries/boost_1_65_1"`
VLD path: `"$(ProgramFiles)/Visual Leak Detector/include"`

## Note 2
`bitmaps/bitmap_group.hpp` -> `bitmaps/bitmap_definition.hpp`
`blamlib/Halo1/` -> `blamlib/`
`Yelolib/Halo1` -> `Yelolib/`
`shared/Include` -> `../source`
`shared/Include/snowhouse/` -> `../external_libraries/snowhouse`
`shared/Include/mongoose` -> `../external_libraries/mongoose`
When files are "moved" from /Halo1/ to parent, `branch:gbuffer_rework` changes are lost. Redo changes!

## Note 3
The "`Blam/yelolib` and dependency move" also deleted `blamlib_Halo2.props`, `blamlib_Halo2.vcxproj.filters`

## Note 4
Check the following files for `const`.
```cpp
#include "Memory/Memorylnterface.hpp' 
#include "Rasterizer/RenderTargetChain.hpp" 
#include "Rasterizer/DX9/rasterizer_dx9_shaders_vshader9.hpp" 
#include "Rasterizer/ShaderExtension/ShaderExtension.hpp' 
#include "Rasterizer/GBuffer/Effects/c_gbuffer_rtcIear_effect.hpp" 
#include 
-> #include "Rasterizer/GBuffer/c_gbuffer_settings.hpp" 
	#pragma region Setting
		class c_settings_container 
			: public Configuration::c_configuration_container 
		public: 
			Configuration::c_configuration_value<bool> m_enabled;
			
			c_settings_container() 
				: Configuration::c_configuration_container("Rasterizer.GBuffer") 
, m_enabledC'Enabled", true) 
protected: 
const std::vector<i_configuration_value* const> GetMembersO final override 
return std::vector<i_configuration_value* const> { &m_enabled h; 
#include "Rasterizer/GBuffer/Effects/c_gbuffer_effect_factory.hpp' 
```

## Note 5
`TagGroups::s_bitmap_group` -> `TagGroups::s_bitmap_definition`
RE: `OpenSauce/Halo1/Halo_CE/Rasterizer/Lightmaps.cpp#L128-L145`
- `branch:gbuffer_rework` moves this to `Render/c_render_device.hpp`

![[FrozenSauce/Main/_Resources/Bitmap_group_to_Bitmap_Definition.png]]

## Note 6
`OpenSauce/Halo1/Halo1_BlamLib/Halo1_BlamLib.vcxproj.filters`
`render_transparent.hpp#L1017`
`sound.hpp#1020`

## Note 7
`OpenSauce/Halo1/Halo1_CE/Game/GameState.cpp` is probably screwed up.
Check it against `Memory/_EngineLayout.inl`.

## Note 8
- Moved blamlib and YeloLib code into `source` directory in root of workspace
- Moved third party code into `external_libraries` in root of workspace

- Action_queue.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/game`
	- `Source/blamlib/game`
- Actor_structures.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/ai`
	- `Source/blamlib/ai`
- Actors.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/ai`
	- `Source/blamlib/ai`
- Ai_communication.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/ai/`
	- `Source/blamlib/ai`
- Ai_script.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/ai/`
	- `source/blamlib/ai/`
- Ai_yelo.cpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/ai/ai_yelo.cpp`
	- `source/YeloLib/ai/ai_yelo.cpp`
- biped_definitions.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/units/biped_definitions.hpp`
	- `source/blamlib/units/biped_definitions.hpp`
- biped_structures.hpp
	- `OpenSauce/shared/Include/blamlib/Halo1/units/biped_structures.hpp`
	- `source/blamlib/units/biped_structures.hpp`
- blam_memory_upgrades.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/open_sauce/blam_memory_upgrades.hpp`
	- `source/YeloLib/open_sauce/blam_memory_upgrades.hpp`
- byte_swapping.cpp
	- `OpenSauce/shared/Include/blamlib/Halo1/memory/byte_swapping.cpp`
	- `source/blamlib/memory/byte_swapping.cpp`
- c_actor_variant_transform_manager.cpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/ai/c_actor_variant_transform_manager.cpp`
	- `source/YeloLib/ai/c_actor_variant_transform_manager.cpp`
- c_actor_variant_transform_manager.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/ai/c_actor_variant_transform_manager.hpp`
	- `source/YeloLib/ai/c_actor_variant_transform_manager.hpp`
- c_interp_base.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/time/interpolation/c_interp_base.hpp`
	- `source/YeloLib/time/interpolation/c_interp_base.hpp`
- c_interp_function.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/time/interpolation/c_interp_function.hpp`
	- `source/YeloLib/time/interpolation/c_interp_function.hpp`
- c_interp_linear.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/time/interpolation/c_interp_linear.hpp`
	- `source/YeloLib/time/interpolation/c_interp_linear.hpp`
- c_lightmap_manager.cpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/render/lightmaps/c_lightmap_manager.cpp`
	- `source/YeloLib/render/lightmaps/c_lightmap_manager.cpp`
- c_lightmap_manager.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/render/lightmaps/c_lightmap_manager.hpp`
	- `source/YeloLib/render/lightmaps/c_lightmap_manager.hpp`
- c_settings_cheape.cpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/open_sauce/settings/c_settings_cheape.cpp`
	- `source/YeloLib/open_sauce/settings/c_settings_cheape.cpp`
- c_settings_cheape.hpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/open_sauce/settings/c_settings_cheape.hpp`
	- `source/YeloLib/open_sauce/settings/c_settings_cheape.hpp`
- c_sky_manager.cpp
	- `OpenSauce/shared/Include/YeloLib/Halo1/render/sky/c_sky_manager.cpp`
	- `source/YeloLib/render/sky/c_sky_manager.cpp`
- c_sky_manager.hpp