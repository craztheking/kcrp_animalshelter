AnimalShelter 1.0v
https://github.com/CrazTheKing

If anyone knows how to add whistle please let me know.

=================================================

Installation :

1 - import database dogs.sql

2 - ensure kcrp_animalshelter

3 - add kcrp_animalshelter folder to resources folder


Usage : 

1. Go to an Animal Shelter on the map, press (E) to open menu, select any horse you like to buy.

2. Call Pet by pressing (J).

3. If your Pet is to far press J (1 time) to reset call event.

=================================================

Current workaround for blip being seen across map:


add


,
	--Animal Shelters
	{ name = 'Animal Shelter', sprite = 1475879922, x = -273.51, y = 689.26, z = 113.41 }

to line 26 , or your last set "ropas" (clothing) coordiante of redm_blips/client.lua

and then remove

local function CreateBlips ( )
	for k,v in pairs(Config.Coords) do
		local blip = Citizen.InvokeNative( 0x554d9d53f696d002, -515518185, v.x, v.y, v.z)
	end
end


from line 108 of kcrp_animalshelter/client.lua


save both, shutdown/reload server.. progress


=================================================
Recreated from:
HORSE SHOP FOR REDEM 0.1v by #mrlupo# / #Proky# / #Plouffe#  
https://github.com/Proky0
https://github.com/mrlupo
https://github.com/mrlupo/elrp_horsedealer
