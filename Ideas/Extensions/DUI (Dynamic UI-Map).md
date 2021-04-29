nToss
> Here's an idea. Dynamic main menu. Rather than pre-defining maps, images, and menu section into a custom main menu (a la UUI), dynamically add them by... A. (Simpler) scanning the maps folder and adding maps to a maps list in the menu. A GUI for mapname. B. (Complex, but better for end users) adding menu buttons and sub-menus via drop-in Lua scripts. The scripts would be written by map authors and used creating menu sections for map packs (custom campaigns, Firefight playlists, et cetera) Optional images (Logos/Banners, map previews) would need to be either in the script file as a blob or as a separate image file in a subdirectory to declutter the menu scripts folder. Now that I think about it, I'd already suggested something similar for TiaraCE…

From <https://discordapp.com/channels/399419085064110082/631949444316659742> 

Kavawuvi 🎀
> @nToss that sounds cool. unfortunately, you just broke the universal UI as well as pretty much other UI map that isn't stock

From <https://discordapp.com/channels/399419085064110082/631949444316659742> 

nToss
> Yayyyy!
> The dynamically-created buttons (Campaign, Firefight, Multiplayer) and their respective submenus would likely need to either replace the stock buttons (assuming the ui author used stock-named tags for button entries) or add them if they are not already present (Add Firefight to a stock-ish ui) To account for tag fuckery, an algorithm would be needed to look for strings within the tags (search for "campaign", "campaña", et cetera) and (optionally) attempt to translate these common strings to other languages. Don't both with long, custom strings provided by map authors. That's their job, not yours/whoever-wants-to-try-implementing this.(edited)
From <https://discordapp.com/channels/399419085064110082/631949444316659742> 
