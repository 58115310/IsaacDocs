# Class "EntityFamiliar"
### Inherits from Class: {: .inheritance }
[Entity](Entity.md)
## Functions
### Add·Coins () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddCoins ( int Value ) {: .copyable aria-label='Functions' }

___ 
### Add·Hearts () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddHearts ( int Hearts ) {: .copyable aria-label='Functions' }

___ 
### Add·Keys () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddKeys ( int Keys ) {: .copyable aria-label='Functions' }

___ 
### Add·To·Delayed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddToDelayed ( ) {: .copyable aria-label='Functions' }
Adds to delayed. This doesn't remove other flags! 
___ 
### Add·To·Followers () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddToFollowers ( ) {: .copyable aria-label='Functions' }
Adds to followers. This doesn't remove other flags! 
___ 
### Add·To·Orbit () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddToOrbit ( int Layer ) {: .copyable aria-label='Functions' }
Adds to orbitals. This doesn't remove other flags! 
___ 
### Fire·Projectile () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [EntityTear](../abp/EntityTear) FireProjectile ( [Vector](../abp/Vector) Dir ) {: .copyable aria-label='Functions' }

Shoots a projectile from the center of the familiar in the direction you defined.
If used on a familiar that shoots multiple projectiles (example: harlequin baby), this function will only return the left most projectile based on the direction. If used on familiars with special tears (example: Lil Brimstone,...), this will just shoot a regular tear.
This function will not play the shoot animation of the familiar.
___ 
### Follow·Parent () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void FollowParent ( ) {: .copyable aria-label='Functions' }

___ 
### Follow·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void FollowPosition ( [Vector](../abp/Vector) Pos ) {: .copyable aria-label='Functions' }

___ 
### Get·Orbit·Distance () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static [Vector](../abp/Vector) GetOrbitDistance ( int Layer ) {: .copyable aria-label='Functions' }

___ 
### Get·Orbit·Position () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) GetOrbitPosition ( [Vector](../abp/Vector) Pos ) {: .copyable aria-label='Functions' }

Returns the position of an orbiting familiar relative to the player's position. Returns `:::lua Vector(0,0) if its a normal familiar.`
The "pos" argument is used as an offset.
___ 
### Move·Delayed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void MoveDelayed ( int NumFrames ) {: .copyable aria-label='Functions' }

___ 
### Move·Diagonally () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void MoveDiagonally ( float Speed ) {: .copyable aria-label='Functions' }

___ 
### Pick·Enemy·Target () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void PickEnemyTarget ( float MaxDistance, int FrameInterval ) {: .copyable aria-label='Functions' }

___ 
### Play·Charge·Anim () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void PlayChargeAnim ( [Direction](../abp/enums/Direction) Dir ) {: .copyable aria-label='Functions' }

___ 
### Play·Float·Anim () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void PlayFloatAnim ( [Direction](../abp/enums/Direction) Dir ) {: .copyable aria-label='Functions' }

___ 
### Play·Shoot·Anim () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void PlayShootAnim ( [Direction](../abp/enums/Direction) Dir ) {: .copyable aria-label='Functions' }

___ 
### Recalculate·Orbit·Offset () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int RecalculateOrbitOffset ( int Layer, boolean Add ) {: .copyable aria-label='Functions' }
Returns the number of familiars in that layer.
___ 
### Remove·From·Delayed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveFromDelayed ( ) {: .copyable aria-label='Functions' }

___ 
### Remove·From·Followers () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveFromFollowers ( ) {: .copyable aria-label='Functions' }

___ 
### Remove·From·Orbit () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveFromOrbit ( ) {: .copyable aria-label='Functions' }

___ 
### Shoot () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void Shoot ( ) {: .copyable aria-label='Functions' }


???+ bug "Bugs"
    This function does not seem to work.
___ 
## Variables
### Coins {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int Coins  {: .copyable aria-label='Variables' }

___ 
### Fire·Cooldown {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int FireCooldown  {: .copyable aria-label='Variables' }

___ 
### Head·Frame·Delay {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int HeadFrameDelay  {: .copyable aria-label='Variables' }

___ 
### Hearts {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int Hearts  {: .copyable aria-label='Variables' }

___ 
### Keys {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int Keys  {: .copyable aria-label='Variables' }

___ 
### Last·Direction {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Direction](../abp/enums/Direction) LastDirection  {: .copyable aria-label='Variables' }

___ 
### Move·Direction {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Direction](../abp/enums/Direction) MoveDirection  {: .copyable aria-label='Variables' }

___ 
### Orbit·Angle·Offset {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float OrbitAngleOffset  {: .copyable aria-label='Variables' }

Can be used to override the angular position of the familiar on its orbit based on the initial starting position of the orbit.

???- example "Example Code"
    This code will make all of your orbitals move as a tight wall around you.

    ```lua 
    for i,v in ipairs(Isaac.GetRoomEntities()) do 
        if v.Type==3 then 
            v:ToFamiliar().OrbitAngleOffset = 0.25*i 
        end 
    end
    ```
    
    Result: ![angle offset](../abp/images/example_familiar_angleOffset.png)
___ 
### Orbit·Distance {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) OrbitDistance  {: .copyable aria-label='Variables' }

Defines the orbit of the familiar, if its an orbital. The Vector is interpreted as the dimensions of the circle/oval orbit. Example: `:::lua Vector(110,90)` is the orbital of "Forever alone".
___ 
### Player {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [EntityPlayer](../abp/EntityPlayer) Player  {: .copyable aria-label='Variables' }

___ 
### Room·Clear·Count {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int RoomClearCount  {: .copyable aria-label='Variables' }

___ 
### Shoot·Direction {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Direction](../abp/enums/Direction) ShootDirection  {: .copyable aria-label='Variables' }

___ 
### State {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int State  {: .copyable aria-label='Variables' }

___ 
