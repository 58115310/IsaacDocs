# Class "Room"
## Functions
### Check·Line () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean CheckLine ( [Vector](../abp/Vector) Pos1, [Vector](../abp/Vector) Pos2, LinecheckMode Mode, int GridPathThreshold, boolean IgnoreWalls, boolean IgnoreCrushable ) {: .copyable aria-label='Functions' }
returns true if there is a direct line of sight between Pos1 and Pos2 returns false if the line is obstructed 

???+ note "Notes"
    Linecheck Modes:

    **0** : makes the line check collide with anything that impedes ground movement

    **1** : is a cheaper version of 0, but is not as reliable

    **2** : is used for explosions, it only collides with walls and indestructible blocks

    **3** : is a line check that only collides with obstacles that can block projectiles
___ 
### Damage·Grid () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean DamageGrid ( int Index, int Damage ) {: .copyable aria-label='Functions' }
Damage Grid Entities currently this concerns [GridEntityPoop](../abp/GridEntityPoop) and GridEntity_Fire returns true if damageable entity was found (and possibly damaged) return false if not used by tears, bombs, some NPCs, etc
___ 
### Destroy·Grid () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean DestroyGrid ( int Index, boolean Immediate ) {: .copyable aria-label='Functions' }
calls DamageGrid internally to damage Poop/Fire removes rocks and opens secret doors returns true if something was destroyed returns false if not used for explosions mostly 
___ 
### Emit·Blood·From·Walls () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void EmitBloodFromWalls ( int Duration, int Count ) {: .copyable aria-label='Functions' }

___ 
### Find·Free·Pickup·Spawn·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) FindFreePickupSpawnPosition ( [Vector](../abp/Vector) Pos, float InitialStep, boolean AvoidActiveEntities ) {: .copyable aria-label='Functions' }
Starting from Pos, will try to find a free spawn position where a newly spawned pickup item will not collide with already spawned pickup items, or solid grid elements such as rocks, or pits The returned position will be aligned to the grid. If no free position is found, the original position (aligned to the grid) is returned. 
___ 
### Find·Free·Tile·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) FindFreeTilePosition ( [Vector](../abp/Vector) Pos, float DistanceThreshold ) {: .copyable aria-label='Functions' }
Finds the nearest free tile based on position Stops immediately if the tile sampled has a squared distance less than DistanceThresholdSQ 
___ 
### Get·Alive·Bosses·Count () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetAliveBossesCount ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Alive·Enemies·Count () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetAliveEnemiesCount ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Award·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetAwardSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Backdrop·Type () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetBackdropType ( ) {: .copyable aria-label='Functions' }

Returns the BackdropType (Background) of the current room.

???- note "BackdropTypes (corresponds to ids in backdrops.xml)"
    
    | ID | Backdrop |
    |--:|:--|
    |1|Basement|
    |2|Cellar|
    |3|Burning Basement|
    |4|Caves|
    |5|Catacombs|
    |6|Drowned Caves|
    |7|Depths|
    |8|Necropolis|
    |9|Dank Depths|
    |10|Womb|
    |11|Utero|
    |12|Scarred Womb|
    |13|Blue Womb (Hush)|
    |14|Sheol|
    |15|Cathedral|
    |16|Dark Room|
    |17|Chest|
    |18|Mega Satan|
    |19|Library|
    |20|Shop|
    |21|Isaacs Room|
    |22|Barren Room|
    |23|Secret Room|
    |24|Dice Room|
    |25|Arcade|
    |26|Error Room|
    |27|Blue Secret|
    |28|Ultra Greed Shop|
___ 
### Get·Boss·ID () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### BossId GetBossID ( ) {: .copyable aria-label='Functions' }

This will return the subtype of the current room, since this value is used to determine the boss-portrait to display when entering.
___ 
### Get·Bottom·Right·Pos () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetBottomRightPos ( ) {: .copyable aria-label='Functions' }
returns bottom right position inside of walls 
___ 
### Get·Broken·Watch·State () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetBrokenWatchState ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Center·Pos () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetCenterPos ( ) {: .copyable aria-label='Functions' }
returns the room center position 
___ 
### Get·Clamped·Grid·Index () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetClampedGridIndex ( [Vector](../abp/Vector) Position ) {: .copyable aria-label='Functions' }
converts float position (x,y) to grid index (similar to ingrid) clamps the values if out of bounds 
___ 
### Get·Clamped·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetClampedPosition ( [Vector](../abp/Vector) Pos, float Margin ) {: .copyable aria-label='Functions' }
returns Pos clamped to room borders inside of walls 
___ 
### Get·Decoration·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetDecorationSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Delirium·Distance () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetDeliriumDistance ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Devil·Room·Chance () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### float GetDevilRoomChance ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [GridEntityDoor](../abp/GridEntityDoor) GetDoor ( [DoorSlot](../abp/enums/DoorSlot) Slot ) {: .copyable aria-label='Functions' data-altreturn='nil' }
Returns the [GridEntityDoor](../abp/GridEntityDoor) at the given [DoorSlot](../abp/enums/DoorSlot) position. Returns nil if no Door is located there.

___ 
### Get·Door·Slot·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetDoorSlotPosition ( [DoorSlot](../abp/enums/DoorSlot) Slot ) {: .copyable aria-label='Functions' }

___ 
### Get·Dungeon·Rock·Idx () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetDungeonRockIdx ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Entities () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [EntityList](../abp/CppContainer_EntityList) GetEntities ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Frame·Count () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetFrameCount ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Grid·Collision () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [GridCollisionClass](../abp/enums/GridCollisionClass) GetGridCollision ( int GridIndex ) {: .copyable aria-label='Functions' }

Returns the [GridCollisionClass](../abp/enums/GridCollisionClass) of the grid entity at this grid index.
___ 
### Get·Grid·Collision·At·Pos () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [GridCollisionClass](../abp/enums/GridCollisionClass) GetGridCollisionAtPos ( [Vector](../abp/Vector) Pos ) {: .copyable aria-label='Functions' }

Returns the [GridCollisionClass](../abp/enums/GridCollisionClass) of the grid entity at this position in the room.
___ 
### Get·Grid·Entity () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [GridEntity](../abp/GridEntity) GetGridEntity ( int Index ) {: .copyable aria-label='Functions' data-altreturn='nil' }

Returns the [GridEntity](../abp/GridEntity) at this grid index. Returns `nil`, when no [GridEntity](../abp/GridEntity) is found.
___ 
### Get·Grid·Entity·From·Pos () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [GridEntity](../abp/GridEntity) GetGridEntityFromPos ( [Vector](../abp/Vector) Position ) {: .copyable aria-label='Functions' data-altreturn='nil' }

Returns the [GridEntity](../abp/GridEntity) at this position in the room. Returns `nil`, when no [GridEntity](../abp/GridEntity) is found.
___ 
### Get·Grid·Height () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetGridHeight ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Grid·Index () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetGridIndex ( [Vector](../abp/Vector) Position ) {: .copyable aria-label='Functions' }
converts float position (x,y) to grid index returns -1 for invalid index 
___ 
### Get·Grid·Path () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetGridPath ( int Index ) {: .copyable aria-label='Functions' }

___ 
### Get·Grid·Path·From·Pos () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetGridPathFromPos ( int Index ) {: .copyable aria-label='Functions' }

___ 
### Get·Grid·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetGridPosition ( int GridIndex ) {: .copyable aria-label='Functions' }
converts grid index to float (x,y) position undefined behaviour for invalid index 
___ 
### Get·Grid·Size () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetGridSize ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Grid·Width () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetGridWidth ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Laser·Target () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetLaserTarget ( [Vector](../abp/Vector) Pos, [Vector](../abp/Vector) Dir ) {: .copyable aria-label='Functions' }
returns the hit position for a laser beam (Technology, Robo-Baby) usually, the first poop, fire, rock, TNT, or wall encountered on a straight line 
___ 
### Get·Lighting·Alpha () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### float GetLightingAlpha ( ) {: .copyable aria-label='Functions' }

___ 
### Get·LRoom·Area·Desc () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### LRoomAreaDesc GetLRoomAreaDesc ( ) {: .copyable aria-label='Functions' }

___ 
### Get·LRoom·Tile·Desc () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### LRoomTileDesc GetLRoomTileDesc ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Next·Shockwave·Id () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetNextShockwaveId ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Random·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetRandomPosition ( float Margin ) {: .copyable aria-label='Functions' }
returns random non tile aligned position 
___ 
### Get·Random·Tile·Index () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetRandomTileIndex ( int Seed ) {: .copyable aria-label='Functions' }

___ 
### Get·Red·Heart·Damage () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean GetRedHeartDamage ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Render·Scroll·Offset () {: aria-label='Functions' }
[ ](#){: .const .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### const [Vector](../abp/Vector) GetRenderScrollOffset ( ) {: .copyable aria-label='Functions' }
The camera scroll offset and screen shake offsets are both represented here. 
___ 
### Get·Render·Surface·Top·Left () {: aria-label='Functions' }
[ ](#){: .const .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### const [Vector](../abp/Vector) GetRenderSurfaceTopLeft ( ) {: .copyable aria-label='Functions' }
The position the floor and wall textures will be rendered at. 
___ 
### Get·Room·Config·Stage () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetRoomConfigStage ( ) {: .copyable aria-label='Functions' }
Returns the stage the room was designed for.

???- note "Stage IDs (corresponds to ids in stages.xml)"
    
    | ID | Backdrop | Notes |
    |--:|:--||
    |0|Special Rooms||
    |1|Basement||
    |2|Cellar||
    |3|Burning Basement||
    |4|Caves||
    |5|Catacombs||
    |6|Drowned Caves||
    |7|Depths||
    |8|Necropolis||
    |9|Dank Depths||
    |10|Womb||
    |11|Utero||
    |12|Scarred Womb||
    |13|Blue Womb (Hush)||
    |14|Sheol||
    |15|Cathedral||
    |16|Dark Room||
    |17|Chest||
    |18|Special Rooms (Greed Mode)||
    |19|Basement (Greed Mode)|Normally inaccessible. In greed mode, the main room is based off of the Special Rooms (Greed Mode) file.|
    |20|Caves (Greed Mode)|Normally inaccessible unless in the first variant of unused stage 13. In greed mode, the main room is based off of the Special Rooms (Greed Mode) file.|
    |21|Depths (Greed Mode)|Normally inaccessible unless in the second variant of unused stage 13. In greed mode, the main room is based off of the Special Rooms (Greed Mode) file.|
    |22|Womb (Greed Mode)|Normally inaccessible unless in the third variant of unused stage 13. In greed mode, the main room is based off of the Special Rooms (Greed Mode) file.|
    |23|Sheol (Greed Mode)|Normally inaccessible. In greed mode, the main room is based off of the Special Rooms (Greed Mode) file.|
    |24|The Shop (Greed Mode)|Normally inaccessible. In greed mode, the main room is based off of the Special Rooms (Greed Mode) file.|
    |25|Ultra Greed (Greed Mode)||
    |26|The Void|Normally inaccessible. This stage uses rooms from other stages, and will return their respective values.|
___ 
### Get·Room·Shape () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [RoomShape](../abp/enums/RoomShape) GetRoomShape ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Second·Boss·ID () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### BossId GetSecondBossID ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Seeded·Collectible () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [CollectibleType](../abp/enums/CollectibleType) GetSeededCollectible ( int Seed ) {: .copyable aria-label='Functions' }

___ 
### Get·Shop·Level () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetShopLevel ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Spawn·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetSpawnSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Tinted·Rock·Idx () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetTintedRockIdx ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Top·Left·Pos () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetTopLeftPos ( ) {: .copyable aria-label='Functions' }
returns top left position inside of walls 
___ 
### Get·Type () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [RoomType](../abp/enums/RoomType) GetType ( ) {: .copyable aria-label='Functions' }

___ 
### Has·Slow·Down () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean HasSlowDown ( ) {: .copyable aria-label='Functions' }

___ 
### Has·Trigger·Pressure·Plates () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean HasTriggerPressurePlates ( ) {: .copyable aria-label='Functions' }

___ 
### Has·Water () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean HasWater ( ) {: .copyable aria-label='Functions' }

___ 
### Has·Water·Pits () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean HasWaterPits ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Ambush·Active () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsAmbushActive ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Ambush·Done () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsAmbushDone ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Clear () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsClear ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Current·Room·Last·Boss () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsCurrentRoomLastBoss ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Door·Slot·Allowed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsDoorSlotAllowed ( [DoorSlot](../abp/enums/DoorSlot) Slot ) {: .copyable aria-label='Functions' }
Returns whether this room design may have a door at a given position, disregarding whether those doors exist. 
___ 
### Is·First·Enemy·Dead () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsFirstEnemyDead ( ) {: .copyable aria-label='Functions' }

___ 
### Is·First·Visit () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsFirstVisit ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Initialized () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsInitialized ( ) {: .copyable aria-label='Functions' }

___ 
### Is·LShaped·Room () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsLShapedRoom ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Position·In·Room () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsPositionInRoom ( [Vector](../abp/Vector) Pos, float Margin ) {: .copyable aria-label='Functions' }

___ 
### Is·Sacrifice·Done () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsSacrificeDone ( ) {: .copyable aria-label='Functions' }

___ 
### Keep·Doors·Closed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void KeepDoorsClosed ( ) {: .copyable aria-label='Functions' }

___ 
### Mama·Mega·Explossion () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void MamaMegaExplossion ( ) {: .copyable aria-label='Functions' }

___ 
### Play·Music () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void PlayMusic ( ) {: .copyable aria-label='Functions' }

___ 
### Remove·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveDoor ( [DoorSlot](../abp/enums/DoorSlot) Slot ) {: .copyable aria-label='Functions' }

___ 
### Remove·Grid·Entity () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveGridEntity ( int GridIndex, int PathTrail, boolean KeepDecoration ) {: .copyable aria-label='Functions' }

___ 
### Render () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void Render ( ) {: .copyable aria-label='Functions' }

___ 
### Respawn·Enemies () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RespawnEnemies ( ) {: .copyable aria-label='Functions' }
for D7 collectible 
___ 
### Screen·Wrap·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) ScreenWrapPosition ( [Vector](../abp/Vector) Pos, float Margin ) {: .copyable aria-label='Functions' }

Returns Pos, screen-wrapped (if it is just outside the room on the right it will be moved to the left side of the room, etc)

???- note "Notes"
     This only wraps the point once, so if it has crossed multiple wrapping planes it will only wrap on the one it's closest to. For wrapping a position that has crossed two planes (outside a room in the top left for instance) call this function iteratively. 
___ 
### Set·Ambush·Done () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetAmbushDone ( boolean Value ) {: .copyable aria-label='Functions' }

___ 
### Set·Broken·Watch·State () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetBrokenWatchState ( int State ) {: .copyable aria-label='Functions' }

___ 
### Set·Card·Against·Humanity () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetCardAgainstHumanity ( ) {: .copyable aria-label='Functions' }

___ 
### Set·Clear () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetClear ( boolean Clear ) {: .copyable aria-label='Functions' }
Needed for angel room, so the clear flag can be set to false when the angel spawns
___ 
### Set·First·Enemy·Dead () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetFirstEnemyDead ( boolean Value ) {: .copyable aria-label='Functions' }

___ 
### Set·Floor·Color () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetFloorColor ( [Color](../abp/Color) FloorColor ) {: .copyable aria-label='Functions' }

Allows you to apply a color modifier to the floor texture of the current room.

???- example "Example Code"
    This code changes the floorcolor to red.
    ```lua 
    Game():GetRoom():SetFloorColor(Color(1,1,1,1,255,0,0))
    ```

___ 
### Set·Grid·Path () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean SetGridPath ( int Index, int Value ) {: .copyable aria-label='Functions' }

___ 
### Set·Red·Heart·Damage () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetRedHeartDamage ( ) {: .copyable aria-label='Functions' }

___ 
### Set·Sacrifice·Done () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetSacrificeDone ( boolean Done ) {: .copyable aria-label='Functions' }

___ 
### Set·Shockwave·Param () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetShockwaveParam ( int ShockwaveId, [ShockwaveParams](../abp/ShockwaveParams) Params ) {: .copyable aria-label='Functions' }

___ 
### Set·Slow·Down () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetSlowDown ( int Duration ) {: .copyable aria-label='Functions' }

___ 
### Set·Wall·Color () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetWallColor ( [Color](../abp/Color) WallColor ) {: .copyable aria-label='Functions' }

Allows you to apply a color modifier to the wall texture of the current room.

???- example "Example Code"
    This code changes the wallcolor to red.
    ```lua 
    Game():GetRoom():SetWallColor(Color(1,1,1,1,255,0,0))
    ```

___ 
### Shop·Reshuffle () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void ShopReshuffle ( boolean KeepCollectibleIdx, boolean ReselectSaleItem ) {: .copyable aria-label='Functions' }

___ 
### Shop·Restock·Full () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void ShopRestockFull ( ) {: .copyable aria-label='Functions' }

___ 
### Shop·Restock·Partial () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void ShopRestockPartial ( ) {: .copyable aria-label='Functions' }

___ 
### Spawn·Clear·Award () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SpawnClearAward ( ) {: .copyable aria-label='Functions' }

___ 
### Spawn·Grid·Entity () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean SpawnGridEntity ( int GridIndex, [GridEntityType](../abp/enums/GridEntityType) Type, int Variant, int Seed, int VarData ) {: .copyable aria-label='Functions' }

___ 
### Try·Make·Bridge () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean TryMakeBridge ( [GridEntity](../abp/GridEntity) pit ) {: .copyable aria-label='Functions' }

___ 
### Try·Place·Ladder () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void TryPlaceLadder ( [Vector](../abp/Vector) PlayerPos, [Vector](../abp/Vector) PlayerVelocity, [Entity](../abp/Entity) Ladder ) {: .copyable aria-label='Functions' }

___ 
### Try·Spawn·Blue·Womb·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean TrySpawnBlueWombDoor ( boolean FirstTime, boolean IgnoreTime ) {: .copyable aria-label='Functions' }

___ 
### Try·Spawn·Boss·Rush·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean TrySpawnBossRushDoor ( boolean IgnoreTime ) {: .copyable aria-label='Functions' }

___ 
### Try·Spawn·Devil·Room·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean TrySpawnDevilRoomDoor ( boolean Animate ) {: .copyable aria-label='Functions' }

___ 
### Try·Spawn·Mega·Satan·Room·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean TrySpawnMegaSatanRoomDoor ( ) {: .copyable aria-label='Functions' }

___ 
### Try·Spawn·The·Void·Door () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean TrySpawnTheVoidDoor ( ) {: .copyable aria-label='Functions' }

___ 
### Turn·Gold () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void TurnGold ( ) {: .copyable aria-label='Functions' }

___ 
### Update () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void Update ( ) {: .copyable aria-label='Functions' }

Updates the current room.

???- note "Notes"
    Calling this function is NOT needed to apply changes!
    This function is pretty useless 
___ 
### World·To·Screen·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) WorldToScreenPosition ( [Vector](../abp/Vector) WorldPos ) {: .copyable aria-label='Functions' }
Converts an entity position to one that can be used to render to the screen. 
___ 
