# Minecraft-PE-Native-Function-Mapping-Table
Minecraft: PE 原生函数与部分字段映射表

此表自用  
_This table is for my person use_

使用和分享此表必须遵守 [CC BY-NC-4.0](LICENSE.zh) 许可证  
_Use and share this table under the [CC BY-NC-4.0](LICENSE) license_

本项目用到了 [libminecraftpe.so-ida-analysis](https://github.com/1503Dev/libminecraftpe.so-ida-analysis/)  
_This project uses [libminecraftpe.so-ida-analysis](https://github.com/1503Dev/libminecraftpe.so-ida-analysis/)_

基本进度:
- [x] ~~1.16.201~~
- [x] 1.16.210
- [x] 1.17.0
- [ ] ~~1.17.41~~
- [ ] ~~1.18.32~~
- [ ] ~~1.19.41~~
- [ ] ~~1.19.83~~
- [ ] ~~1.20.0~~
- [ ] ~~1.20.15~~
- [ ] ~~1.20.41~~
- [ ] 1.20.81
- [ ] 1.21.2
- [ ] ...

# Content
- [Minecraft-PE-Native-Function-Mapping-Table](#minecraft-pe-native-function-mapping-table)
- [Content](#content)
- [Table](#table)
  - [1.16.201.01\_arm64-v8a](#11620101_arm64-v8a)
    - [AABB](#aabb)
    - [Abilities](#abilities)
    - [Actor](#actor)
    - [Camera](#camera)
    - [ClientInstance](#clientinstance)
    - [GameMode](#gamemode)
    - [GuiData](#guidata)
    - [Level](#level)
    - [LevelRendererPlayer](#levelrendererplayer)
    - [LocalPlayer](#localplayer)
    - [Minecraft](#minecraft)
    - [MinecraftGame](#minecraftgame)
    - [Mob](#mob)
    - [MobEffectInstance](#mobeffectinstance)
    - [Player](#player)
    - [PlayerRewindContext](#playerrewindcontext)
    - [PlayerSnapshot](#playersnapshot)
    - [Timer](#timer)
  - [1.16.210.05\_arm64-v8a](#11621005_arm64-v8a)
    - [Abilities](#abilities-1)
    - [Actor](#actor-1)
    - [ActorEventCoordinator](#actoreventcoordinator)
    - [BossComponent](#bosscomponent)
    - [BlockPosTrackerComponent](#blockpostrackercomponent)
    - [ClientInstance](#clientinstance-1)
    - [ClientNetworkHandler](#clientnetworkhandler)
    - [EffectCommand](#effectcommand)
    - [EntityContextBase](#entitycontextbase)
    - [FunctionManager](#functionmanager)
    - [GameMode](#gamemode-1)
    - [GuiData](#guidata-1)
    - [InGamePlayScreen](#ingameplayscreen)
    - [ItemUseInventoryTransaction](#itemuseinventorytransaction)
    - [Level](#level-1)
    - [LevelRendererPlayer](#levelrendererplayer-1)
    - [LocalPlayer](#localplayer-1)
    - [Minecraft](#minecraft-1)
    - [MobEffectInstance](#mobeffectinstance-1)
    - [MobEvents](#mobevents)
    - [NetworkIdentifier](#networkidentifier)
    - [OwnerStorageEntity](#ownerstorageentity)
    - [Player](#player-1)
    - [ServerLevel](#serverlevel)
    - [ServerNetworkHandler](#servernetworkhandler)
    - [ServerPlayer](#serverplayer)
    - [SurvivalMode](#survivalmode)
    - [Timer](#timer-1)
    - [UpdatePlayerGameTypePacket](#updateplayergametypepacket)
  - [1.17.0.02\_arm64-v8a](#117002_arm64-v8a)
    - [Abilities](#abilities-2)
    - [Actor](#actor-2)
    - [ClientInstance](#clientinstance-2)
    - [GameMode](#gamemode-2)
    - [GuiData](#guidata-2)
    - [InGamePlayScreen](#ingameplayscreen-1)
    - [Level](#level-2)
    - [LevelRendererPlayer](#levelrendererplayer-2)
    - [LocalPlayer](#localplayer-2)
    - [Minecraft](#minecraft-2)
    - [MobEffectInstance](#mobeffectinstance-2)
    - [Player](#player-2)
    - [SurvivalMode](#survivalmode-1)
    - [Timer](#timer-2)
  - [1.17.41.01\_arm64-v8a](#1174101_arm64-v8a)
    - [Abilities](#abilities-3)
    - [Actor](#actor-3)
    - [ClientInstance](#clientinstance-3)
    - [GameMode](#gamemode-3)
    - [GuiData](#guidata-3)
    - [LocalPlayer](#localplayer-3)
    - [MobEffectInstance](#mobeffectinstance-3)
    - [Player](#player-3)
  - [1.21.2.02\_arm64-v8a](#121202_arm64-v8a)
    - [Abilities](#abilities-4)
    - [Actor](#actor-4)
    - [ClientInstance](#clientinstance-4)
    - [GameMode](#gamemode-4)
    - [ItemStack](#itemstack)
    - [Level](#level-3)
    - [LevelRendererPlayer](#levelrendererplayer-3)
    - [Minecraft](#minecraft-3)
    - [MinecraftGame](#minecraftgame-1)
    - [MobEffectInstance](#mobeffectinstance-4)
    - [Player](#player-4)

# Table
## 1.16.201.01_arm64-v8a
- jint **JNI_OnLoad** (JavaVM* vm, void* reserved)  
  `0x41A6BDC`

### AABB
- AABB* **AABB::expand** (Vec3 const& direction)  
  `0x5F97FE8`

### Abilities
- _void **Abilities::Abilities** (Abilities* this)_  
  `0x642157C`
- bool **Abilities::getBool** (int index)  
  `0x6423020`

### Actor
- void **Actor::addEffect** (const MobEffectInstance* mobEffectInstance)  
  `0x6688354`
- bool **Actor::canFly** ()  
  `0x6676940`
- bool **Actor::canPowerJump** ()  
  `0x6676A90`
- float **Actor::distanceTo** (Actor* target)  
  `0x66750AC`
- std::vector\<DistanceSortedActor\> **Actor::fetchNearbyActorsSorted** (const Vec3& position, ActorType type)  
  `0x668D148`
- AABB* **Actor::getAABBShapeComponent** ()  
  `0x666BB94`
- float **Actor::getCameraDistance** () const  
  `0x66882C4`
- Vec3* **Actor::getPos** ()  
  `0x666EBCC`
- bool **Actor::getStatusFlag** (ActorFlags flag) const  
  `0x666B670`
- bool **Actor::isAlive** ()  
  `0x66785FC`
- bool **Actor::isLocalPlayer** ()  
  `0x66785D4`
- void **Actor::setCanFly** (bool canFly)  
  `0x6676968`
- void **Actor::setPos** (const Vec3* pos)  
  `0x666E938`

### Camera
- Vec3* **Camera::getPosition** ()  
  `0x55F0C14`

### ClientInstance
- GuiData* **ClientInstance::getGuiData** ()  
  `0x55198C8`
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x5510B58`
- bool **ClientInstance::isInGame** ()  
  `0x55177A4`
- void **ClientInstance::requestLeaveGame** (bool immediateExit, bool suppressConfirmation)  
  `0x550C414`
- void **ClientInstance::tick** ()  
  `0x550E108`
- bool **ClientInstance::update** (bool forceUpdate)  
  `0x550E1F0`

### GameMode
- bool **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0x634D43C`
- float **GameMode::getMaxPickRange** ()  
  `0x634F960`
- bool **GameMode::startDestroyBlock** (const BlockPos& pos, unsigned char face, bool& outResult)  
  `0x634CFCC`

### GuiData
- void **GuiData::displayClientMessage** (std::string const& message)  
  `0x541E76C`
- void **GuiData::setActionBarMessage** (std::string const& message)  
  `0x5420B20`
- void **GuiData::setGuiScale** (float scale)  
  `0x5420718`
- void **GuiData::setSubtitle** (std::string const& message)  
  `0x5420A5C`
- void **GuiData::setTitle** (std::string const& message)  
  `0x54209D4`
- void **GuiData::showTipMessage** (std::string const& message)  
  `0x541F844`

### Level
- bool **Level::destroyBlock** (BlockSource& source, const BlockPos& pos, bool dropResources)  
  `0x61BD3B8`
- std::vector\<Actor\*> **Level::getRuntimeActorList** () const  
  `0x61BDAA4`
- void **Level::tick** ()  
  `0x61B4C50`

### LevelRendererPlayer
- float **LevelRendererPlayer::getFov** (float baseFov, bool useSmoothTransition)  
  `0x5999834`

### LocalPlayer
- void **LocalPlayer::addLevels** (int levels)  
  `0x5BA7658`
- float **LocalPlayer::getPickRange** ()  
  `0x5BA7B5C`
- bool **LocalPlayer::isFlying** ()  
  `0x5BA27E0`
- void **LocalPlayer::jumpFromGround** ()  
  `0x5BA7C98`
- void **LocalPlayer::setPlayerGameType** (GameType type)  
  `0x5BA5C5C`
- void **LocalPlayer::setPlayerGameTypeWithoutServerNotification** (GameType type)  
  `0x5BA5D14`
- void **LocalPlayer::setPos** (Vec3 const& pos)  
  `0x5BA2DFC`

### Minecraft
- Timer* **Minecraft::getTimer** ()  
  `0x6A24930`
- void **Minecraft::setGameModeReal** (GameType type)  
  `0x6A23344`
- void **Minecraft::update** ()  
  `0x6A23390`

### MinecraftGame
- void* **MinecraftGame::getInput** ()  
  `0x5572D5C`
- void **MinecraftGame::tickInput** ()  
  `0x5561998`

### Mob
- bool **Mob::isSprinting** ()  
  `0x6643C84`

### MobEffectInstance
- _void **MobEffectInstance::MobEffectInstance** (MobEffectInstance\* this, unsigned int effectId, int durationTicks, int level, bool b1, bool effectVisible, bool b2)_  
  `0x63B73F0`

### Player
- bool **Player::attack** (Actor* target)  
  `0x6438CE0`
- float **Player::getAttackDamage** ()  
  `0x643E2C0`
- float **Player::getCameraOffset** ()  
  `0x6437E10`
- GameType **Player::getPlayerGameType** ()  
  `0x643F78C`
- float **Player::getSpeed** ()  
  `0x642C3B4`

### PlayerRewindContext
- bool **PlayerRewindContext::isOnGround** ()  
  `0x5C4C2E8`
- bool **PlayerRewindContext::isSprinting** ()  
  `0x5C4D128`

### PlayerSnapshot
- _void **PlayerSnapshot::PlayerSnapshot** (PlayerSnapshot\* this)_  
  `0x5650584`

### Timer
- int **mTicksPerSecond**  
  `+0x0` ?
  
   ---
- _void **Timer::Timer** (Timer* this)_  
  `0x421A85C`
- float **Timer::getTimeScale** ()  
  `0x421A970`
- void **Timer::setTimeScale** (float scale)  
  `0x421A980`

## 1.16.210.05_arm64-v8a
_此表未经完全验证_

- jint **JNI_OnLoad** (JavaVM\* vm, void\* reserved)  
  `0x1DA1A20`

### Abilities
- bool **Abilities::getBool** (AbilitiesIndex index)  
  `0x281D644`

### Actor
- bool **mIsAlive**  
  `+0x3A9`
- Level **mLevel**  
  `+0x350`
- Vec3 **mPos**  
  `+0x590`

  ---
- void **Actor::addEffect** (const MobEffectInstance* mobEffectInstance)  
  `0x24ED9C4`
- float **Actor::distanceTo** (Actor const&)  
  `0x24DA18C`
- Level* **Actor::getLevel** ()  
  `0x24CA2A4`
- Vec3* **Actor::getPos** ()  
  `0x24D15D4`
- void* **Actor::getUniqueID** ()  
  `0x24CEA00`
- bool **Actor::isAlive** ()  
  `0x24DD7F4`
- void **Actor::remove** ()  
  `0x24D48D0`
- void **Actor::setPos** (const Vec3* pos)  
  `0x24D3CF0`

### ActorEventCoordinator
- void **ActorEventCoordinator::sendActorRemoved** (Actor*)  
  `0x21659C4`

### BossComponent
- void **BossComponent::unRegisterPlayer** (Actor*, Player*)  
  `0x1BFE344`

### BlockPosTrackerComponent
- void **BlockPosTrackerComponent::onRemove** (Actor*)  
  `0x5A1B3D4`

### ClientInstance
- GuiData* **mGuiData**  
  `+0x4B0` ?
- LocalPlayer* **mLocalPlayer**  
  `+0x118`

  ---
- void **ClientInstance::_updateScreenSizeVariables** (Vec2 const&, float, float, float)  
  `0x34B64E4`
- DateManager* **ClientInstance::getDateManager** ()  
  `0x34BBF58`
- GuiData* **ClientInstance::getGuiData** ()  
  `0x34BBF40` ?
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x34B0FE0`
- bool **ClientInstance::isInGame** ()  
  `0x34B99D4`
- void **ClientInstance::requestLeaveGame** (bool immediateExit, bool suppressConfirmation)  
  `0x34B99C4`
- void **ClientInstance::setClientGameMode** (GameType type)  
  `0x34C195C`
- void **ClientInstance::startExternalNetworkWorld** (Social::GameConnectionInfo, std::string const&, bool)  
  `0x34AC780`
- void **ClientInstance::update** (bool forceUpdate)  
  `0x34AE5BC`

### ClientNetworkHandler
- void **ClientNetworkHandler::handle** (const NetworkIdentifier *, const SetTitlePacket *)  
  `0x37E3A48`
- void **ClientNetworkHandler::handle** (const NetworkIdentifier *, const TextPacket *)  
  `0x37DB9FC` ?
- void **ClientNetworkHandler::handle** (const NetworkIdentifier *, const UpdatePlayerGameTypePacket *)  
  `0x37DDA70`

### EffectCommand
- void **EffectCommand::execute** (const CommandOrigin \*, CommandOutput \*)  
  `0x1FD00F4`

### EntityContextBase
- **EntityContextBase::_enttRegistry** ()  
  `0x1D2DB18`

### FunctionManager
- void **FunctionManager::tick** ()  
  `0x1DFCB30`

### GameMode
- bool **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0x20EB8C0`
- float **GameMode::getMaxPickRange** ()  
  `0x20EDC78`

### GuiData
- void **GuiData::displayClientMessage** (std::string const& message)  
  `0x3310FB4`
- void **GuiData::setActionBarMessage** (std::string const& message)  
  `0x3313E5C`
- void **GuiData::setGuiScale** (float scale)  
  `0x3313A58` ?
- void **GuiData::setSubtitle** (std::string const& message)  
  `0x3313D98`
- void **GuiData::setTitle** (std::string const& message)  
  `0x3313D10`
- void **GuiData::showTipMessage** (std::string const& message)  
  `0x3312AB0`

### InGamePlayScreen
- float? **InGamePlayScreen::_getPickRange** ()
  `0x3395128`
- void **InGamePlayScreen::_renderItemInHand** (ScreenContext *, Player *)  
  `0x3396490`
- void **InGamePlayScreen::applyInput** (float)  
  `0x33918FC`

### ItemUseInventoryTransaction
- void **ItemUseInventoryTransaction::handle** (Player*, bool)  
  `0x20D329C`

### Level
- void **Level::tick** ()  
  `0x2E9DCE0`

<!-- ### LevelChunk
- std::vector<Actor*>*? **LevelChunk::getEntities** ()  
  `0x2B65DF4` -->

### LevelRendererPlayer
- float **LevelRendererPlayer::getFov** (float baseFov, bool useSmoothTransition)  
  `0x3FACD44`

### LocalPlayer
- void **LocalPlayer::addLevels** (int levels)  
  `0x3700B9C`
- void **LocalPlayer::displayClientMessage** (std::string const& message)  
  `0x36FBEB0`
- float? **LocalPlayer::getPickRange** ()  
  `0x37010B4`
- void **LocalPlayer::jumpFromGround** ()  
  `0x37011F0`
- void **LocalPlayer::resetRot** ()  
  `0x36FACD0`
- void **LocalPlayer::setPlayerGameType** (GameType type)  
  `0x36FE0E0`
- void **LocalPlayer::setPlayerGameTypeWithoutServerNotification** (GameType type)  
  `0x36FE198`
- void **LocalPlayer::setPos** (const Vec3* pos)  
  `0x36FACA4`
- void **LocalPlayer::startRiding** (Actor *)  
  `0x37000EC`
- void **LocalPlayer::stopSpinAttack** ()  
  `0x36FBE2C`

### Minecraft
- Timer **mTimer**  
  `+0xB8`

  ---
- void **Minecraft::getTimer** ()  
  `0x289421C`
- void **Minecraft::setGameModeReal** (GameType type)  
  `0x28929FC`

### MobEffectInstance
- _**MobEffectInstance::MobEffectInstance** (MobEffectInstance* this, unsigned int effectId, int durationTicks, int level, bool b1, bool effectVisible, bool b2)_  
  `0x21637D4`
- bool **MobEffectInstance::operator!=** (MobEffectInstance const&)  
  `0x2164324`

### MobEvents
- void **MobEvents::tick** ()  
  `0x2EAD348`

### NetworkIdentifier
- bool **NetworkIdentifier::equalsTypeData** (NetworkIdentifier const&)  
  `0x17F2D4C`

### OwnerStorageEntity
- **OwnerStorageEntity::_getStackRef** ()  
  `0x17B3DD0`
- **OwnerStorageEntity::_hasValue** ()  
  `0x17B3C14`

### Player
- void **Player::attack** (Actor *)  
  `0x2834044`
- float **Player::getCameraOffset** ()  
  `0x2832D5C`
- GameType **Player::getPlayerGameType** ()  
  `0x283AEAC`
- int **Player::getClientSubId** ()  
  `0x28266EC`
- float **Player::getSpeed** ()  
  `0x2826BFC`
- void **Player::setPlayerGameType** (GameType type)  
  `0x283A66C`

### ServerLevel
- void **ServerLevel::tick** ()
  `0x1E11794`

### ServerNetworkHandler
- void **ServerNetworkHandler::handle** (Level \*\*this, const NetworkIdentifier\* networkIdentifier, const InteractPacket\* packet)  
  `0x1921758`

### ServerPlayer
- bool **ServerPlayer::isValidTarget** (Actor*)  
  `0x1E16384`
- void **ServerPlayer::sendMobEffectPackets** ()  
  `0x1E1CDA0` 
- void **ServerPlayer::setPlayerGameType** (Actor* actor, GameType type)  
  `0x1E1CD08`
- void **ServerPlayer::tickWorld** (Tick const&)  
  `0x1E13A74`

### SurvivalMode
- void **SurvivalMode::destroyBlock** (const BlockPos *, unsigned __int8)  
  `0x20EE4BC`

### Timer
- int **mTicksPerSecond**  
  `+0x0` ?

### UpdatePlayerGameTypePacket
- _void **UpdatePlayerGameTypePacket::UpdatePlayerGameTypePacket** (UpdatePlayerGameTypePacket* this, GameType gameType, ActorUniqueID const& actorUniqueId)_  
  `0x1F00390`

## 1.17.0.02_arm64-v8a
_此表未经完全验证_

- jint **JNI_OnLoad** (JavaVM\* vm, void\* reserved)  
  `0x191146C`

### Abilities
- bool **Abilities::getBool** (AbilitiesIndex index)  
  `0x2B68E58`

### Actor
- bool **mIsAlive**  
  `+0x3C1`
- Level **mLevel**  
  `+0x368`
- Vec3 **mPos**  
  `+0x5F8`

  ---
- void **Actor::addEffect** (MobEffectInstance const&)  
  `0x2850A34`
- float **Actor::distanceTo** (Actor const&)  
  `0x283CBE4`
- Level* **Actor::getLevel** ()  
  `0x282ADC8`
- Vec3* **Actor::getPos** ()  
  `0x2833654`
- void* **Actor::getUniqueId** ()  
  `0x2830B88`
- bool **Actor::isAlive** ()  
  `0x2840110`
- void **Actor::remove** ()  
  `0x2836E40`
- void **Actor::setPos** (Vec3 const&)  
  `0x2836218`

### ClientInstance
- GuiData **mGuiData**  
  `+0x4B0`
- LocalPlayer **mLocalPlayer**  
  `+0x118`

  ---
- void **ClientInstance::_updateScreenSizeVariables** (Vec2 const&, float, float, float)  
  `0x3A2A0FC`
- GuiData* **ClientInstance::getGuiData** ()  
  `0x3A302CC`
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x3A24588`
- bool **ClientInstance::isInGame** ()  
  `0x3A2D6B8` ?
- void **ClientInstance::requestLeaveGame** (bool immediateExit, bool suppressConfirmation)  
  `0x3A1F628`
- void **ClientInstance::startExternalNetworkWorld** (Social::GameConnectionInfo, std::string const&, bool)  
  `0x3A24598`
- void **ClientInstance::update** (bool forceUpdate)  
  `0x3A215E0`

### GameMode
- void **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0x2449258`
- float **GameMode::getMaxPickRange** ()  
  `0x244B600`

### GuiData
- UNKNOWN **mScreenSizeData**  
  `+0x14`

  ---
- void **GuiData::displayClientMessage** (std::string const& message)  
  `0x387F328`
- void* **GuiData::getScreenSizeData** ()  
  `0x3880DF0`
- void **GuiData::setActionBarMessage** (std::string const& message)  
  `0x38821D8`
- void **GuiData::setGuiScale** (float scale)  
  `0x3881DD4`
- void **GuiData::setSubtitle** (std::string const& message)  
  `0x3882114`
- void **GuiData::setTitle** (std::string const& message)  
  `0x388208C`
- void **GuiData::showTipMessage** (std::string const& message)  
  `0x3880E24`

### InGamePlayScreen
- float? **InGamePlayScreen::_getPickRange** ()  
  `0x3906A30`
- void **InGamePlayScreen::applyInput** (float)  
  `0x3902A30`

### Level
- void **Level::tick** ()  
  `0x32CE0BC`

### LevelRendererPlayer
- float **LevelRendererPlayer::getFov** (float baseFov, bool useSmoothTransition)  
  `0x45A39FC`

### LocalPlayer
- void **LocalPlayer::addLevels** (int levels)  
  `0x3D0510C`
- void **LocalPlayer::displayClientMessage** (std::string const& message)  
  `0x3D015FC`
- float **LocalPlayer::getPickRange** ()  
  `0x3D0560C`
- void **LocalPlayer::jumpFromGround** ()  
  `0x3D05750`
- void **LocalPlayer::resetRot** ()  
  `0x3CFF414`
- void **LocalPlayer::setPlayerGameType** (GameType type)  
  `0x3D036BC`
- void **LocalPlayer::setPlayerGameTypeWithoutServerNotification** (GameType type)  
  `0x3D03774`
- void **LocalPlayer::setPos** (Vec3 const& pos)  
  `0x3CFF3E8`
- void **LocalPlayer::startRiding** (Actor *)  
  `0x3D04660`

### Minecraft
- Timer **mTimer**  
  `+0xC8`

  ---
- void **Minecraft::getTimer** ()  
  `0x2AFC328`

### MobEffectInstance
- _**MobEffectInstance::MobEffectInstance** (MobEffectInstance \* this, unsigned int, int, int, bool, bool, bool)_  
  `0x24BDD18`

### Player
- void **Player::attack** (Actor *)  
  `0x2B7F898`
- float **Player::getCameraOffset** ()  
  `0x2B7E65C`
- GameType **Player::getPlayerGameType** ()  
  `0x2B8697C`
- float **Player::getSpeed** ()  
  `0x2B724BC`
- void **Player::setPlayerGameType** (GameType type)  
  `0x2B86124`

### SurvivalMode
- void **SurvivalMode::destroyBlock** (BlockPos const&, unsigned char)  
  `0x244BE38`

### Timer
- int **mTicksPerSecond**  
  `+0x0` ?

## 1.17.41.01_arm64-v8a
_此表未经完全验证_
- jint **JNI_OnLoad** (JavaVM\* vm, void\* reserved)  
  `0x37AA618`

### Abilities
- bool **Abilities::getBool** (AbilitiesIndex index)  
  `0x4D8F314`

### Actor
- bool **mIsAlive**  
  `+0x3B9` ?
- Level **mLevel**  
  `+0x360`
- Vec3 **mPos**  
  `+0x620`
- UNKNOWN **mRuntimeID**  
  `+0x518`
- char **mUniqueId**  
  `+0x248`

  ---
- void **Actor::addEffect** (MobEffectInstance const&)  
  `0x3DE80A0`
- float **Actor::distanceTo** (Actor const&)  
  `0x3DD5A7C`
- Level* **Actor::getLevel** ()  
  `0x3DC28A8`
- Vec3* **Actor::getPos** ()  
  `0x3DCBB74`
- void* **Actor::getRuntimeID** ()  
  `0x3DC828C`
- char* **Actor::getUniqueId** ()  
  `0x3DC8300`
- bool **Actor::isAlive** ()  
  `0x3DD94B4` ?
- bool **Actor::isSneaking** ()  
  `0x3DCDCA8`
- void **Actor::remove** ()  
  `0x3DCFB00`
- void **Actor::setPos** (Vec3 const& pos)  
  `0x3DCEA4C`
- void **Actor::setRot** (Vec2 const& rot)  
  `0x3DCFFF0`

### ClientInstance
- GuiData **mGuiData**  
  `+0x4C0`
- LocalPlayer **mLocalPlayer**  
  `+0x118`

  ---
- GuiData* **ClientInstance::getGuiData** ()  
  `0x55282A4`
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x551C878 `
- bool **ClientInstance::isInGame** ()  
  `0x552567C` ?
- void **ClientInstance::requestLeaveGame** (bool immediateExit, bool suppressConfirmation)  
  `0x55175A4`
- void **ClientInstance::startExternalNetworkWorld** (Social::GameConnectionInfo, std::string const&, bool)  
  `0x551C9A0`
- void **ClientInstance::update** (bool forceUpdate)  
  `0x55195F4`

### GameMode
- void **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0x484A2D8`
- float **GameMode::getMaxPickRange** ()  
  `0x484C770`
- float **GameMode::getPickRange** (InputMode const&, bool)  
  `0x484C6D4`
- void **GameMode::startDestroyBlock** (BlockPos const& pos, unsigned char, bool)  
  `0x4849E9C`

### GuiData
- float **mGuiScale**  
  `+0x30`
- float **mGuiScaleActual**  
  `+0x34`

  ---
- void **GuiData::setGuiScale** (float scale)  
  `0x61AD1AC`

### LocalPlayer
- void **LocalPlayer::setPos** (Vec3 const& pos)  
  `0x3CEF174`

### MobEffectInstance
- _**MobEffectInstance::MobEffectInstance** (MobEffectInstance \* this, unsigned int, int, int, bool, bool, bool)_  
  `0x57C4018`

### Player
- ItemStack **Player::getSelectedItem** ()  
  `0x4D9C748`
- void **Player::setPlayerGameType** (GameType type)  
  `0x4DADD94`

## 1.21.2.02_arm64-v8a
_此表未经完全验证_

- jint **JNI_OnLoad** (JavaVM\* vm, void\* reserved)  
  `0xC6F7C9C`

### Abilities
- bool **Abilities::getBool** (AbilitiesIndex index)  
  `0xA8B37B0`

### Actor
- void **Actor::addEffect** (MobEffectInstance const&)  
  `0xAB127C0`
- float **Actor::distanceTo** (Actor const&)  
  `0xAAFED0C`
- float **Actor::distanceTo** (Vec3 const&)  
  `0xAAFED5C`
- Level* **Actor::getLevel** ()  
  `0xAAED1B4`
- Vec3* **Actor::getPosition** ()  
  `0xAAEFB44`
- bool **Actor::isAlive** ()  
  `0xAB016EC`
- void **Actor::setPos** (Vec3 const& pos)  
  `0xAAF6514`
- void **Actor::teleportTo** (Vec3 const&, bool, int, int, ActorUniqueID const&)  
  `0x627F600`

### ClientInstance
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x62828E4`
- void **ClientInstance::update** (bool forceUpdate)  
  `0x6282944`

### GameMode
- void **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0xA722810`
- float **GameMode::getMaxPickRange** ()  
  `0xA725E10`

### ItemStack
- void **ItemStack::ItemStack** (std::string_view name, int count, int aux, CompoundTag const\* tag)  
  `0xB5BF368`

### Level
- bool **Level::isMultiplayerGame** ()  
  `0xB15A948`
- void **Level::tick** ()  
  `0xDE57D50`

### LevelRendererPlayer
- float **LevelRendererPlayer::getFov** (float, bool)  
  `0x73F4264`

### Minecraft
- Timer **mTimer**
  `+0xD0`

  ---
- UNKNOWN* **Minecraft::getEntityRegistry** ()  
  `0xAB8F828`

### MinecraftGame
- void **MinecraftGame::onClientLevelExit** ()  
  `0x61F0BDC`

### MobEffectInstance
- _**MobEffectInstance::MobEffectInstance** (MobEffectInstance \* this, unsigned int, int, int, bool, bool, bool)_  
  `0xA77086C`

### Player
- void **Player::add** (ItemStack const&)  
  `0xA851770`
- GameMode **Player::getGameMode** ()  
  `0xA860B10`
- float **Player::getSpeed** ()  
  `0xA849608`
- void **Player::teleportTo** (Vec3 const&, bool, int, int, ActorUniqueID const&)  
  `0xA849114`