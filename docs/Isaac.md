---
tags:
  - 全局
  - 类
  - Isaac
---
# 类 "Isaac"

???+ info "提示"
    **访问Isaac类的方法时，需要使用`.`（句点）而不是`:`（冒号）！**

    例如：
    ```lua
    local player = Isaac.GetPlayer()
    ```

## 函数
### Add·Callback () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void AddCallback ( table modRef, function callbackId, table callbackFn, int entityId ) {: .copyable aria-label='Functions' }
添加一个MOD回调。

推荐使用[Mod Reference](ModReference.md)的[AddCallback](ModReference.md#addcallback)函数而非该函数。

___
### Add·Pill·Effect·To·Pool () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int AddPillEffectToPool ( int pillEffect ) {: .copyable aria-label='Functions' }
将一个胶囊效果pillEffect加入到胶囊池中。

返回胶囊颜色。

___
### Add·Priority·Callback () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void AddPriorityCallback ( table modRef, function callbackId, [CallbackPriority](enums/CallbackPriority.md) priority, table callbackFn, int entityId ) {: .copyable aria-label='Functions' }
添加一个MOD回调。该回调具有优先级，并根据优先级决定执行顺序。

推荐使用[Mod Reference](ModReference.md)的[AddPriorityCallback](ModReference.md#addcallback)函数而非该函数。

___
### Console·Output () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void ConsoleOutput ( string text ) {: .copyable aria-label='Functions' }

向控制台打印一行文本。

???- example "示例代码"
    你可以使用该示例作为替代。
    ```lua
    Isaac.ConsoleOutput("This is a Test.")
    -- 输出: This is a Test.

    -- 替代:
    print("This is a Test.")
    -- 输出: This is a Test.

    ```

___
### Count·Bosses () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int CountBosses ( ) {: .copyable aria-label='Functions' }

返回本房间内的头目数量。
___
### Count·Enemies () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int CountEnemies ( ) {: .copyable aria-label='Functions' }

返回本房间内的敌人数量。
___
### Count·Entities () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### int CountEntities ( [Entity](Entity.md) Spawner, [EntityType](enums/EntityType.md) Type = EntityType.ENTITY_NULL, int Variant = -1, int SubType = -1 ) {: .copyable aria-label='Functions' }

返回本房间内的满足指定需求的实体数量。

Spawner为该实体的创建者。（可以为`:::lua nil`）

Type为该实体的类型。（可以为`:::lua EntityType.ENTITY_NULL`）

Variant和SubType为该实体的变体和子类型。（可以为`:::lua -1`）

___
### Debug·String () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void DebugString ( string str ) {: .copyable aria-label='Functions' }

向日志文件打印一行文本。你可以在这里找到文件：`:::lua %systemdrive%\Users\%username%\Documents\My Games\Binding of Isaac Repentance\log.txt`

???- example "示例代码"
    这行代码会向log.txt打印`:::lua "This is a Test."`。
    ```lua
    Isaac.DebugString("This is a Test.")
    -- Output: [INFO] - Lua Debug: This is a Test.

    ```

___
### Execute·Command () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### string ExecuteCommand ( string command ) {: .copyable aria-label='Functions' }

执行一个控制台指令。

关于如何使用指令，见[控制台教程](tutorials/DebugConsole.md)。
___
### Explode () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void Explode ( [Vector](Vector.md) pos, [Entity](Entity.md) source, float damage ) {: .copyable aria-label='Functions' }

在pos位置生成一次爆炸。其伤害源实体为source，伤害为damage。
___
### Find·By·Type () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### table FindByType ( [EntityType](enums/EntityType.md) Type, int Variant = -1, int SubType = -1, boolean Cache = false, boolean IgnoreFriendly = false ) {: .copyable aria-label='Functions' }
返回符合Type，Variant和SubType的所有实体。

如果Variant/SubType为-1，表示包括任意Variant/SubType的实体。

Cache为true时会缓存结果，一帧执行多次时可以使用。
___
### Find·In·Radius () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### table FindInRadius ( [Vector](Vector.md) Position, float Radius, int Partitions = 0xFFFFFFFF  ) {: .copyable aria-label='Functions' }
返回中心为Position，半径为Radius范围内的所有由Partitions筛选的实体（另见[EntityPartition enum](enums/EntityPartition.md)）（包括所有 = 0xffffffff）

该函数不根据实体距离中心的距离，而是根据他们加载的顺序排序。
___
### Get·Built·In·Callback·State () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### boolean GetBuiltInCallbackState ( function callbackId ) {: .copyable aria-label='Functions' }
获取内置回调状态。

作用未知。
___
### Get·Callbacks () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### table GetCallbacks ( function callbackId, boolean createIfMissing ) {: .copyable aria-label='Functions' }
获取所有callbackId的MOD回调。

createIfMissing：为true时，如果没有该回调，则创建一个。
___
### Get·Card·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetCardIdByName ( string cardHudName ) {: .copyable aria-label='Functions' }
基于“pocketitems.xml”文件中定义的“hud”属性返回[卡牌ID](enums/Card.md) 。如果找不到具有该“hud”属性值的卡，则返回`-1`。

???+ warning "警告"
    该函数的名称具有误导性，该函数只能使用卡片的“hud”属性值，而不能使用卡牌的名称。

???+ bug "漏洞"
    此函数不适用于原版卡片/符文，因为它们在pocketitems.xml文件中的条目中没有定义“hud”属性。您需要使用[Card](enums/Card.md)枚举来获取原版的ID。

???- example "示例代码"
    以下代码获取一张MOD卡牌的卡牌ID。
    ```xml
    <pocketitems>
        <card type="tarot" pickup="1" description="some description"  name="My new card" hud="my_modded_card" />
    </pocketitems>
    ```
    ```lua
    Isaac.GetCardIdByName("my_modded_card")
    ```

___
### Get·Challenge () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetChallenge ( ) {: .copyable aria-label='Functions' }
返回玩家当前正在进行的挑战的ID。如果玩家没有进行任何挑战，则返回0。
___
### Get·Challenge·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetChallengeIdByName ( string challengeName ) {: .copyable aria-label='Functions' }

根据挑战的名称返回挑战的ID。（文件：challenges.xml）如果找不到具有该名称的挑战，则返回`-1`（区分大小写）。

???- example "示例代码"
    以下代码获取挑战“愚人节”的挑战ID。
    ```lua
    Isaac.GetChallengeIdByName("Aprils fool")
    --返回：32

    ```

___
### Get·Costume·Id·By·Path () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetCostumeIdByPath ( string path ) {: .copyable aria-label='Functions' }

根据外观的文件路径返回外观的ID。（文件：costumes2.xml）如果找不到具有该路径的外观，则返回`-1`。

???- example "示例代码"
    以下代码获取套装“拉了！”的外观ID。
    ```lua
    Isaac.GetCostumeIdByPath("gfx/characters/n027_Transformation_Poop.anm2")
    --返回：27

    ```

___
### Get·Curse·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetCurseIdByName ( string curseName ) {: .copyable aria-label='Functions' }

根据诅咒的名称返回诅咒的ID。（文件：curses.xml）如果找不到具有该名称的诅咒，则返回`-1`。

???- example "示例代码"
    以下代码获取未知诅咒的诅咒ID。
    ```lua
    Isaac.GetCurseIdByName("Curse of the Unknown")
    --返回：4

    ```

___
### Get·Entity·Type·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetEntityTypeByName ( string entityName ) {: .copyable aria-label='Functions' }

根据实体的名称返回实体的EntityType。（文件：entities2.xml）如果找不到具有该名称的实体，则返回`0`。

???- note "注意"
    没有该函数的SubType版本。

???- example "示例代码"
    以下代码获取燃烧裂口尸的EntityType。
    ```lua
    Isaac.GetEntityTypeByName("Flaming Gaper")
    --返回：10

    ```

___
### Get·Entity·Variant·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetEntityVariantByName ( string entityName ) {: .copyable aria-label='Functions' }

根据实体的名称返回实体的Variant。（文件：entities2.xml）如果找不到具有该名称的实体，则返回`-1`。

???- note "注意"
    没有该函数的SubType版本。

???- example "示例代码"
    以下代码获取燃烧裂口尸的Variant。

    ```lua
    Isaac.GetEntityVariantByName("Flaming Gaper")
    --返回：2

    ```

___
### Get·Frame·Count () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetFrameCount ( ) {: .copyable aria-label='Functions' }

返回整个游戏正在运行的帧数。即使游戏暂停或在主菜单中，计数器也会增加！

1秒大致等于60帧。

因此，此函数的工作方式与`:::lua Game():GetFrameCount()`[Link](Game.md#GetFrameCount)截然不同。

___
### Get·Free·Near·Position () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) GetFreeNearPosition ( [Vector](Vector.md) pos, float step ) {: .copyable aria-label='Functions' }

返回距离位置pos最近的空区域。
___
### Get·Item·Config () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [ItemConfig](ItemConfig.md) GetItemConfig ( ) {: .copyable aria-label='Functions' }

获取ItemConfig对象。

这是唯一可以访问`ItemConfig`对象的方法。
___
### Get·Item·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetItemIdByName ( string itemName ) {: .copyable aria-label='Functions' }

根据道具名称返回道具的ID。（文件：items.xml）如果找不到具有该名称的道具，则返回`-1`。

???- example "示例代码"
    以下代码获取一个MOD道具的ID。
    ```xml
    <passive id="1" name="My Mod Item" description="some description" gfx="my_modded_item.png"/>
    ```
    ```lua
    Isaac.GetItemIdByName("My Mod Item")
    ```

___
### Get·Music·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetMusicIdByName ( string musicName ) {: .copyable aria-label='Functions' }

返回一个音乐的ID。（文件：music.xml）如果找不到具有该名称的音乐，则返回`-1`。

???- example "示例代码"
    以下代码获取标题界面的音乐ID。

    ```lua
    Isaac.GetMusicIdByName("Title Screen")
    --返回：61

    ```

___
### Get·Pill·Effect·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetPillEffectByName ( string pillEffect ) {: .copyable aria-label='Functions' }

根据胶囊效果的名称返回胶囊效果ID。（文件：pocketitems.xml）如果找不到具有该名称的胶囊效果，则返回`-1`。

???- example "示例代码"
    以下代码获取“我能永远看清！”的胶囊效果ID。

    ```lua
    Isaac.GetPillEffectByName("I can see forever!")
    --返回：23

    ```

___
### Get·Player () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### [EntityPlayer](EntityPlayer.md) GetPlayer ( int playerID = 0 ) {: .copyable aria-label='Functions' data-altreturn='nil' }

返回与提供的玩家ID匹配的EntityPlayer。玩家ID从0开始并向上递增。例如，当扮演雅各布和以扫时，雅各布的玩家ID将为0，以扫的玩家ID为1。

如果传递了无效的玩家ID（例如-20或20），则函数将假定玩家索引为0。

如果在任何玩家初始化之前调用此函数（即在主菜单中调用它），则此函数会返回`nil`。

此函数与[`Game():GetPlayer()`](Game.md#GetPlayer)相同。

???- example "示例代码"

    ```lua
    local function getPlayers()
      local game = Game()
      local numPlayers = game:GetNumPlayers()

      local players = {}
      for i = 0, numPlayers - 1 do
        local player = Isaac.GetPlayer(i)
        table.insert(players, player)
      end

      return players
    end
    ```

___
### Get·Player·Type·By·Name () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### [PlayerType](enums/PlayerType.md) GetPlayerTypeByName ( string playerName , boolean Tainted = false ) {: .copyable aria-label='Functions' }

根据角色的名称返回角色类型（ID）。（文件：players.xml）如果找不到具有该名称的角色，则返回`-1`。

???- example "示例代码"
    以下代码获取阿撒泻勒的角色类型。

    ```lua
    Isaac.GetPlayerTypeByName("Azazel")
    --返回：7

    ```

___
### Get·Random·Position () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) GetRandomPosition ( ) {: .copyable aria-label='Functions' }

返回当前房间内的随机位置。

返回值是一个向量，表示世界坐标中的位置。
___
### Get·Room·Entities () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### table GetRoomEntities ( ) {: .copyable aria-label='Functions' }

返回一个可迭代表，该表包含调用函数时房间中的所有实体。

此行为不同于[`Room::GetEntities()`](Room.md#GetEntities)，后者返回一个原始指针，指向在任何给定时间存储房间所有实体的数组。

**对于大多数用例，建议使用[`Isaac.GetRoomEntities（）`](Isaac.md#getroomnentities)！**

???- example "示例代码"
    以下代码打印房间中每个实体的Type、Variant和SubType。

    ```lua
    for i, entity in ipairs(Isaac.GetRoomEntities()) do
        print(entity.Type, entity.Variant, entity.SubType)
    end

    ```

___
### Get·Screen·Height () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### float GetScreenHeight ( ) {: .copyable aria-label='Functions' }

获取游戏屏幕的高度（以像素为单位）。
___
### Get·Screen·Point·Scale () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### float GetScreenPointScale ( ) {: .copyable aria-label='Functions' }

返回一个表示屏幕“缩放”程度的数字。

根据游戏窗口的分辨率，可以是`1.0`或`2.0`等。

???- example "视频演示"
    <figure class="video_container">
        <video controls="true" allowfullscreen="true" muted="true" style="width:25rem">
            <source src="../customData/screen-point-scale.mp4" type="video/mp4">
        </video>
        <figcaption>演示游戏窗口的大小如何改变此函数返回的值。</figcaption>
    </figure>

___
### Get·Screen·Width () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### float GetScreenWidth ( ) {: .copyable aria-label='Functions' }

获取游戏屏幕的宽度（以像素为单位）。
___
### Get·Sound·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetSoundIdByName ( string soundName ) {: .copyable aria-label='Functions' }

根据音效的名称返回音效的ID。（文件：sounds.xml）如果找不到具有该名称的音效，则返回`-1`。

???- example "示例代码"
    以下代码获取名为"Custom Sound Effect"的音效ID。

    ```lua
    Isaac.GetSoundIdByName("Custom Sound Effect")

    ```

___
### Get·Text·Width () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetTextWidth ( string str ) {: .copyable aria-label='Functions' }

基于“terminus8”字体（与Isaac.RenderText()中使用的字体相同），返回给定字符串的宽度（以像素为单位）。

___
### Get·Time () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetTime ( ) {: .copyable aria-label='Functions' }

返回自计算机操作系统启动以来的当前时间（以毫秒为单位）。

这与经过了多少帧无关，对于测量经过了多少实时时间非常有用。（帧并不是一个很好的时间指标，因为游戏会在每层过渡动画和房间过渡动画时加载新数据，然后锁定。）

例如，您可以使用它来实现基于实时的屏幕速度运行计时器，或者将一个函数的性能影响与另一个函数进行比较。

___
### Get·Trinket·Id·By·Name () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### int GetTrinketIdByName ( string trinketName ) {: .copyable aria-label='Functions' }

根据饰品的名称返回其饰品ID。（文件：items.xml）如果找不到具有该名称的饰品，则返回`-1`。

???- example "示例代码"
    以下代码获取一个MOD饰品的ID。
    ```xml
    <trinket id="1" name="My Mod Trinket" description="some description" gfx="my_modded_trinket.png"/>
    ```
    ```lua
    Isaac.GetTrinketIdByName("My Mod Trinket")
    ```

___
### Grid·Spawn () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [GridEntity](GridEntity.md) GridSpawn ( [GridEntityType](enums/GridEntityType.md) gridEntityType, int variant, [Vector](Vector.md) position, boolean forced ) {: .copyable aria-label='Functions' }

在给定位置（世界坐标）生成一个[网格实体](GridEntity.md)。

???+ bug "Bugs"
    “forced”参数无效，并且将**不会**覆盖给定位置的网格实体。如果必要的话，先在在给定位置移除网格实体，然后在再其上生成新的网格实体。

例如，要在房间中央生成一块超级标记石头：

```lua
local game = Game()
local room = game:GetRoom()
local centerPos = room:GetCenterPos()
Isaac.GridSpawn(GridEntityType.GRID_ROCK_SS, 0, centerPos, true)
```

___
### Has·Mod·Data () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### boolean HasModData ( table modRef ) {: .copyable aria-label='Functions' }

如果您的mod使用“SaveModData()”函数存储了数据——换句话说，如果你的mod的数据文件夹中有一个“saveX.dat”文件，则返回`true`。

有3个“saveX.dat”文件，每个存档一个。数字表示它对应的存档，由游戏自动确定。

对于AB+，它们存储在“main.lua”文件旁边的mod文件夹中。

对于忏悔，它们存储在游戏文件中“mods”文件夹旁边的“data”文件夹中。

建议使用[Mod Reference](ModReference.md#hasdata)的[HasData](ModReference.md#HasData)函数而非该函数。
___
### Load·Mod·Data () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### string LoadModData ( table modRef ) {: .copyable aria-label='Functions' }

返回使用“SaveModData()”函数存储在“saveX.dat”文件中的字符串。如果您的mod的数据中没有“saveX.dat”文件，此函数将返回一个空字符串。

有3个“saveX.dat”文件，每个存档一个。数字表示它对应的存档，由游戏自动确定。

如果在主菜单中调用此函数，默认情况下，它将返回存档1的保存数据。

对于AB+，它们存储在“main.lua”文件旁边的mod文件夹中。

对于忏悔，它们存储在游戏文件中“mods”文件夹旁边的“data”文件夹中。

建议使用[Mod Reference](ModReference.md#hasdata)的[LoadData](ModReference.md#HasData)函数而非该函数。
___
### Register·Mod () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void RegisterMod ( table modRef, string modName, int apiVersion ) {: .copyable aria-label='Functions' }

在游戏中注册一个表以使用[Mod Reference](ModReference.md)。

建议改用全局的[RegisterMod](GlobalFunctions.md#RegisterMod)函数。

___
### Remove·Callback () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void RemoveCallback ( table modRef, function callbackId, table callbackFn ) {: .copyable aria-label='Functions' }

移除一个MOD回调。

推荐使用[Mod Reference](ModReference.md)的[RemoveCallback](ModReference.md#addcallback)函数而非该函数。

___
### Remove·Mod·Data () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void RemoveModData ( table modRef ) {: .copyable aria-label='Functions' }

如果存在储存的“saveX.dat”文件，将其删除。

有3个“saveX.dat”文件，每个存档一个。数字表示它对应的存档，由游戏自动确定。

建议使用[Mod Reference](ModReference.md#hasdata)的[RemoveData](ModReference.md#HasData)函数而非该函数。
___
### Render·Scaled·Text () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void RenderScaledText ( string str, float X, float Y, float ScaleX, float ScaleY, float R, float G, float B, float A ) {: .copyable aria-label='Functions' }

在屏幕上渲染缩放后的文本。X和Y坐标需要在屏幕坐标（X[0，~500) Y[0，~350) ）中。ScaleX、ScaleY、R、G、B和A需要在[0,1]之间。

某些比例值可能会导致字体显示变形和像素化。

???- example "示例代码"
    以下代码在屏幕上显示玩家的位置。

    ```lua
    local player = Isaac.GetPlayer()
    local text = "X: " .. player.Position.X .. ", Y: " .. player.Position.Y
    Isaac.RenderScaledText(text, 50, 50, 0.5, 0.5, 1, 1, 1, 1)
    ```

___
### Render·Text () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void RenderText ( string str, float X, float Y, float R, float G, float B, float A ) {: .copyable aria-label='Functions' }

在屏幕上渲染默认大小的文本。X和Y坐标需要在屏幕坐标（X[0，~500) Y[0，~350) ）中。ScaleX、ScaleY、R、G、B和A需要在[0,1]之间。

???- example "示例代码"
    以下代码在屏幕上显示玩家的位置。

    ```lua
    local player = Isaac.GetPlayer()
    local pos = player.Position
    Isaac.RenderText("X: "..pos.X.." Y: "..pos.Y, 50, 50, 1 ,1 ,1 ,1 )

    ```

___
### Run·Callback () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void RunCallback ( function callbackId, ... ) {: .copyable aria-label='Functions' }

执行所有callbackId的MOD回调。
___
### Run·Callback·With·Param () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void RunCallbackWithParam ( function callbackId, object param, ... ) {: .copyable aria-label='Functions' }

执行所有可选参数为param的callbackId的MOD回调。
___
### Save·Mod·Data () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### void SaveModData ( table modRef, string data ) {: .copyable aria-label='Functions' }

向“saveX.dat”存储一串字符串。存储的数据在重开一局和游戏重启之后也会存在，因此非常适合存储持久数据。

有3个“saveX.dat”文件，每个存档一个。数字表示它对应的存档，由游戏自动确定。

对于AB+，它们存储在“main.lua”文件旁边的mod文件夹中。

对于忏悔，它们存储在游戏文件中“mods”文件夹旁边的“data”文件夹中。

建议使用[Mod Reference](ModReference.md#hasdata)的[SaveData](ModReference.md#HasData)函数而非该函数。
___
### Screen·To·World () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) ScreenToWorld ( [Vector](Vector.md) pos ) {: .copyable aria-label='Functions' }

将屏幕坐标（也称为窗口坐标）转换为世界坐标。这可以用于根据屏幕上的某一点获取房间中的特定位置。

世界坐标为x[0，inf) y[0，inf)。
___
### Screen·To·World·Distance () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) ScreenToWorldDistance ( [Vector](Vector.md) pos ) {: .copyable aria-label='Functions' }
___
### Set·Built·In·Callback·State () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void SetBuiltInCallbackState ( function callbackId, boolean state ) {: .copyable aria-label='Functions' }

设置内置回调状态。

作用未知。
___

### Spawn () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Entity](Entity.md) Spawn ( int entityType, int entityVariant, int entitySubtype, [Vector](Vector.md) position, [Vector](Vector.md) velocity, [Entity](Entity.md) Spawner ) {: .copyable aria-label='Functions' }

在给定位置生成一个实体。如果位置不是空的，会在最近的空位置生成。

有两个生成实体的函数：[Isaac.Spawn()](Isaac.md#Spawn)和[Game():Spawn()](Game.md#Spawn)。如果你需要用特定的种子来生成实体，那么你可以使用[Game():Spawn()](Game.md#Spawn)。如果你想生成随机种子的实体，那么你可以使用[Isaac.Spawn()](Isaac.md#Spawn)。

大多数情况下，会使用[Isaac.Spawn()](Isaac.md#Spawn)。

???- example "示例代码"
    以下代码在本房间的中央生成一个随机道具。
    ```lua
    Isaac.Spawn(EntityType.ENTITY_PICKUP, PickupVariant.PICKUP_COLLECTIBLE, 0, Vector(320,280), Vector(0,0), nil)

    ```
___
### World·To·Render·Position () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) WorldToRenderPosition ( [Vector](Vector.md) pos ) {: .copyable aria-label='Functions' }

将世界坐标（又名游戏坐标）转换为渲染坐标。这可以用于在房间中的固定位置渲染事物。渲染坐标系为x[0，inf) y[0，inf)。它定义当前房间中渲染平面上的位置。

???- example "示例代码"
    以下代码在鼠标光标的位置渲染“Test”，与游戏是否处于全屏无关。
    ```lua
    local mousePos = Input.GetMousePosition(true)
    local renderpos = Isaac.WorldToRenderPosition(mousePos) * 2
    Isaac.RenderText("test", renderpos.X, renderpos.Y, 1 ,1 ,1 ,1 )
    ```

___
### World·To·Screen () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) WorldToScreen ( [Vector](Vector.md) pos ) {: .copyable aria-label='Functions' }

将世界坐标（又名游戏坐标）转换为屏幕（又名窗口）坐标。这可以用来渲染实体旁边的东西。屏幕坐标系为x[0，inf) y[0，inf)。通常情况下，它一直到~500x ~300y。

返回值向量包含整数值或以.5结尾的数字。

???- example "示例代码"
    以下代码在角色的位置渲染“Test”，会跟随角色移动。
    ```lua
    local player = Isaac.GetPlayer()
    local screenpos = Isaac.WorldToScreen(player.Position)
    Isaac.RenderText("test", screenpos.X, screenpos.Y, 1 ,1 ,1 ,1 )

    ```

___
### World·To·Screen·Distance () {: aria-label='Functions' }
[ ](#){: .abrep .tooltip .badge }
#### [Vector](Vector.md) WorldToScreenDistance ( [Vector](Vector.md) pos ) {: .copyable aria-label='Functions' }

___
