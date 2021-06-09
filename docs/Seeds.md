# Class "Seeds"
## Functions
### Add·Seed·Effect () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void AddSeedEffect ( [SeedEffect](../abp/enums/SeedEffect) Value ) {: .copyable aria-label='Functions' }

___ 
### Can·Add·Seed·Effect () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean CanAddSeedEffect ( [SeedEffect](../abp/enums/SeedEffect) Value ) {: .copyable aria-label='Functions' }

___ 
### Clear·Seed·Effects () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void ClearSeedEffects ( ) {: .copyable aria-label='Functions' }

___ 
### Clear·Start·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void ClearStartSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Count·Seed·Effects () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int CountSeedEffects ( ) {: .copyable aria-label='Functions' }

___ 
### Count·Unlocked·Seed·Effects () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static int CountUnlockedSeedEffects ( ) {: .copyable aria-label='Functions' }

___ 
### Forget·Stage·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void ForgetStageSeed ( [LevelStage](../abp/enums/LevelStage) Stage ) {: .copyable aria-label='Functions' }

___ 
### Get·Next·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetNextSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Player·Init·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetPlayerInitSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Seed·Effect () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static [SeedEffect](../abp/enums/SeedEffect) GetSeedEffect ( string str ) {: .copyable aria-label='Functions' }

___ 
### Get·Stage·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetStageSeed ( [LevelStage](../abp/enums/LevelStage) Stage ) {: .copyable aria-label='Functions' }

___ 
### Get·Start·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### int GetStartSeed ( ) {: .copyable aria-label='Functions' }

___ 
### Get·Start·Seed·String () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### string GetStartSeedString ( ) {: .copyable aria-label='Functions' }

___ 
### Has·Seed·Effect () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean HasSeedEffect ( [SeedEffect](../abp/enums/SeedEffect) Value ) {: .copyable aria-label='Functions' }

___ 
### Init·Seed·Info () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static InitSeedInfo ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Custom·Run () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsCustomRun ( ) {: .copyable aria-label='Functions' }
Returns true if the player is in a challenge run or a seeded run.
___ 
### Is·Initialized () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsInitialized ( ) {: .copyable aria-label='Functions' }

___ 
### Is·Seed·Combo·Banned () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### boolean IsSeedComboBanned ( [SeedEffect](../abp/enums/SeedEffect) Seed1, [SeedEffect](../abp/enums/SeedEffect) Seed2 ) {: .copyable aria-label='Functions' }

___ 
### Is·Special·Seed () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static boolean IsSpecialSeed ( string str ) {: .copyable aria-label='Functions' }

___ 
### Is·String·Valid·Seed () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static boolean IsStringValidSeed ( string str ) {: .copyable aria-label='Functions' }

___ 
### Remove·Blocking·Seed·Effects () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveBlockingSeedEffects ( [SeedEffect](../abp/enums/SeedEffect) Value ) {: .copyable aria-label='Functions' }
Removes seeds that are banned in conjunction with the given seed. 
___ 
### Remove·Seed·Effect () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void RemoveSeedEffect ( [SeedEffect](../abp/enums/SeedEffect) Value ) {: .copyable aria-label='Functions' }

___ 
### Reset () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void Reset ( ) {: .copyable aria-label='Functions' }
Removes all seed effects, only goes into effect when the run is restarted
___ 
### Restart () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void Restart ( [Challenge](../abp/enums/Challenge) CurrentChallenge ) {: .copyable aria-label='Functions' }
Re-selects a random start seed but only if the start seed was not custom. 
___ 
### Seed2String () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static string Seed2String ( int seed ) {: .copyable aria-label='Functions' }

___ 
### Set·Start·Seed () {: aria-label='Functions' }
[ ](#){: .abp .tooltip .badge }
#### void SetStartSeed ( string StartSeed ) {: .copyable aria-label='Functions' }
Empty string means we will pick a new random seed. 
___ 
### String2Seed () {: aria-label='Functions' }
[ ](#){: .static .tooltip .badge } [ ](#){: .abp .tooltip .badge }
#### static int String2Seed ( string str ) {: .copyable aria-label='Functions' }
___ 
