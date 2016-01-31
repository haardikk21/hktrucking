# Locations

## Syntax
The mission location enums follow the following code pattern

	ID,
	LoadName[128],
	Float:LoadX,
	Float:LoadY,
	Float:LoadZ,
	Float:UnloadX,
	Float:UnloadY,
	Float:UnloadZ,
	Pay
	
## What You Need to Change
LoadX - It is the X coordinate of the location from where the mission will start
LoadY - It is the Y coordinate of the location from where the mission will start
LoadZ - It is the Z coordinate of the location from where the mission will start

UnloadX - It is the X coordinate of the location where the mission will end
UnloadY - It is the Y coordinate of the location where the mission will end
UnloadZ - It is the Z coordinate of the location where the mission will end

Pay (Default is 5000) - The amount of money the trucker will receive upon successful completion of the mission.

## The Code File
This code starts from line number 1288

	new MisLocations[][MisLocationsEnum] =
	{
		{0, "Mission 1",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{1, "Mission 2",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{2, "Mission 3",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{3, "Mission 4",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{4, "Mission 5",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{5, "Mission 6",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{6, "Mission 7",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{7, "Mission 8",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{8, "Mission 9",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{9, "Mission 10",0.3,0.3,0.3,0.3,0.3,0.3,5000}
	};
	new BusLocations[][BusLocationsEnum] =
	{
		{0, "Mission 1",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{1, "Mission 2",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{2, "Mission 3",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{3, "Mission 4",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{4, "Mission 5",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{5, "Mission 6",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{6, "Mission 7",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{7, "Mission 8",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{8, "Mission 9",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{9, "Mission 10",0.3,0.3,0.3,0.3,0.3,0.3,5000}
	};
	new TaxiLocations[][TaxiLocationsEnum] =
	{
		{0, "Mission 1",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{1, "Mission 2",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{2, "Mission 3",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{3, "Mission 4",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{4, "Mission 5",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{5, "Mission 6",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{6, "Mission 7",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{7, "Mission 8",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{8, "Mission 9",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{9, "Mission 10",0.3,0.3,0.3,0.3,0.3,0.3,5000}
	};
	new PilotLocations[][PilotLocationsEnum] =
	{
		{0, "Mission 1",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{1, "Mission 2",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{2, "Mission 3",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{3, "Mission 4",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{4, "Mission 5",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{5, "Mission 6",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{6, "Mission 7",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{7, "Mission 8",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{8, "Mission 9",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{9, "Mission 10",0.3,0.3,0.3,0.3,0.3,0.3,5000}
	};
	new BoatLocations[][BoatLocationsEnum] =
	{
		{0, "Mission 1",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{1, "Mission 2",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{2, "Mission 3",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{3, "Mission 4",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{4, "Mission 5",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{5, "Mission 6",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{6, "Mission 7",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{7, "Mission 8",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{8, "Mission 9",0.3,0.3,0.3,0.3,0.3,0.3,5000},
		{9, "Mission 10",0.3,0.3,0.3,0.3,0.3,0.3,5000}
	};
