# Class "ProjectileParams"
## Constructors
### Projectile·Params () {: aria-label='Constructors' }
[ ](#){: .abp .tooltip .badge }
#### [ProjectileParams](../abp/ProjectileParams) ProjectileParams ( ) {: .copyable aria-label='Constructors' }

___ 
## Variables
### Acceleration {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float Acceleration  {: .copyable aria-label='Variables' }

___ 
### Bullet·Flags {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int BulletFlags  {: .copyable aria-label='Variables' }

___ 
### Change·Flags {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int ChangeFlags  {: .copyable aria-label='Variables' }

Uses [ProjectileFlags](../abp/enums/ProjectileFlags) to define the projectile attributes after the "Changed" state was activated.
The [ProjectileFlag](../abp/enums/ProjectileFlags).CHANGE_FLAGS_AFTER_TIMEOUT needs to be set to allow for this change to apply!
____
**Informations about "Changed" State:**

Projectiles can have two states: normal (default) and changed.


Changed state activates when projectile's frame count reaches the value set in [ChangeTimeout](#ChangeTimeout). After that its flags get changed to what was set in [ChangeFlags](#ChangeFlags) and velocity will be resized to length set in [ChangeVelocity](#ChangeVelocity).
____
Also used in: [EntityProjectile](../abp/EntityProjectile)
___ 
### Change·Timeout {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int ChangeTimeout  {: .copyable aria-label='Variables' }

Number of frames that need to elapse after spawn till the "Changed" state is activated.
The [ProjectileFlag](../abp/enums/ProjectileFlags).CHANGE_FLAGS_AFTER_TIMEOUT or CHANGE_VELOCITY_AFTER_TIMEOUT need to be set to allow for this change to apply!
____
**Informations about "Changed" State:**

Projectiles can have two states: normal (default) and changed.


Changed state activates when projectile's frame count reaches the value set in [ChangeTimeout](#ChangeTimeout). After that its flags get changed to what was set in [ChangeFlags](#ChangeFlags) and velocity will be resized to length set in [ChangeVelocity](#ChangeVelocity).
____
Also used in: [EntityProjectile](../abp/EntityProjectile)
___ 
### Change·Velocity {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float ChangeVelocity  {: .copyable aria-label='Variables' }

Velocity value that gets applied when the "Changed" state is activated.
The [ProjectileFlag](../abp/enums/ProjectileFlags).CHANGE_VELOCITY_AFTER_TIMEOUT need to be set to allow for this change to apply!
____
**Informations about "Changed" State:**

Projectiles can have two states: normal (default) and changed.


Changed state activates when projectile's frame count reaches the value set in [ChangeTimeout](#ChangeTimeout). After that its flags get changed to what was set in [ChangeFlags](#ChangeFlags) and velocity will be resized to length set in [ChangeVelocity](#ChangeVelocity).
____
Also used in: [EntityProjectile](../abp/EntityProjectile)
___ 
### Circle·Angle {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float CircleAngle  {: .copyable aria-label='Variables' }
Angle offset used by fire_projectiles PROJECTILES_CIRCLE type emitter. Random by default. 
___ 
### Curving·Strength {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float CurvingStrength  {: .copyable aria-label='Variables' }
Use very small values for curving like 0.005. 
___ 
### Depth·Offset {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float DepthOffset  {: .copyable aria-label='Variables' }

___ 
### Dot·Product·Limit {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float DotProductLimit  {: .copyable aria-label='Variables' }
Direction bullets are being fired in Dot product of FireDirectionLimit, bullet direction must be &gt;= this value 
___ 
### Falling·Accel·Modifier {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float FallingAccelModifier  {: .copyable aria-label='Variables' }

___ 
### Falling·Speed·Modifier {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float FallingSpeedModifier  {: .copyable aria-label='Variables' }

___ 
### Fire·Direction·Limit {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) FireDirectionLimit  {: .copyable aria-label='Variables' }

___ 
### Grid·Collision {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### boolean GridCollision  {: .copyable aria-label='Variables' }

___ 
### Height·Modifier {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float HeightModifier  {: .copyable aria-label='Variables' }

___ 
### Homing·Strength {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float HomingStrength  {: .copyable aria-label='Variables' }
Multiplier on normal homing strength. Unused if SMART bullet flag is not set. 
___ 
### Color {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Color](../abp/Color) Color  {: .copyable aria-label='Variables' }

___ 
### Position·Offset {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) PositionOffset  {: .copyable aria-label='Variables' }

___ 
### Scale {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float Scale  {: .copyable aria-label='Variables' }

___ 
### Spread {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float Spread  {: .copyable aria-label='Variables' }
For quad/quint/etc spread shots. 
___ 
### Target·Position {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### [Vector](../abp/Vector) TargetPosition  {: .copyable aria-label='Variables' }

___ 
### Variant {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int Variant  {: .copyable aria-label='Variables' }

___ 
### Velocity·Multi {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### float VelocityMulti  {: .copyable aria-label='Variables' }

___ 
### Wiggle·Frame·Offset {: aria-label='Variables' }
[ ](#){: .abp .tooltip .badge }
#### int WiggleFrameOffset  {: .copyable aria-label='Variables' }
Used to offset the wiggle wave. 
___ 
