# all-races-coop-maps

1. сделать переменными ( убрать constant checkbox)
 PLAYER_01_USER = 1 <Integer>
 PLAYER_02_USER = 2 <Integer>

2. в Init 03 Players инициализировать игрока 1 и 2
        Variable -Set PLAYER_01_USER = (Player 1 from (Get Allied Commanders Players()))
        General -If (Conditions) then do (Actions) else do (Actions)
            If
                (Number of players in (Get Allied Commanders Players())) > 1
            Then
                Variable -Set PLAYER_02_USER = (Player 2 from (Get Allied Commanders Players()))
            Else
                Variable -Set PLAYER_02_USER = PLAYER_01_USER (изменено)

3. изменить игроков 3/4/5(пример из miner ecacuation) 
   PLAYER_03_AMON_Claimers = 13 <Integer (Constant)>
   PLAYER_04_AMON_BaseWaves = 14 <Integer (Constant)>
   PLAYER_05_INFESTED_Bullies/Holdout/NeutralToss = 12 <Integer (Constant)>

 оставить загрузку только для игроков 1-5

4. убедится что удален триггер "defeat base dead"

5. Run Victory / Run Defeat нужно убедится что используются Victory/Defeat из модуля Mission(COOP)

 меняешь владельца предстуановленных юнитов игроков 3-5

Player Start 1 - Player Start 5

6. установить точки старта игроков

точки старта амуна Amon Start 1 - Amon Start 2

точка старта игрока будет Player Start <количество игроков>-<номер игрока>, а если нет Player Start <номер игрока> (изменено)

точка старта игрока за Амуна будет Amon Start <количество игроков за амуна>-<номер игрока>, а если нет Amon Start <номер игрока>
НОВОЕ

Optional Zone 1      -    Optional Zone 5    опциональные ресы, юниты для определенного количества игроков командиров

Optional Zone 2-1      Optional Zone 2-2     опициональные ресы для определенного количества игроков амуна

иногда удобно использовать Clear Zone <колво игроков> чтобы удалить ресы

Safety Zone - безопасная о мутаторов зона при любом колве игроков
Safety Zone 1    -     Safety Zone 5     - дополнительные безопасные зоны при конкретном количестве игроков
при игре на 1 . либо 1 экспаншен либо 2 если они в разных сторонах , при игре на 4 игроков одна из экспаншенов амуна будет появлятся. при игре на 5 оба экспаншена амуна .
Initial Exploration [<колво игроков>]    это зона на которой иргоки видят где их экспаншены

при желании предустановить юнитов здания для трех стандартных рас (теры , протоссы зерги )


тут есть список типов предустанавливаемых юнитов COOPAIReplacement
Изображение
ситоит проверить на картах что все юниты заменяются
Изображение
"Doodads Replacement Area"
удалить refinery/assimilators/extractors и рабочих амуна
а еще на основные базы амуна с минералами добавь защитников. например парочку доминаторов)
Изображение
Изображение
Evil <номер маршрута>-<точка на маршруте>
Evil 1-1  , Evil 1-2    -  первый маршрут
Evil 2-1, Evil 2-2  - второй маршрут

## install

git clone hometlt/all-races-coop-maps <SC2Directory>/Maps/coop

## Template


Dependencies:
 - bnet:ARC MOD/0.0/201728,file:Mods\ARC.SC2Mod

Map Properties:
 Info:
  Name: [ARC] <Map Name>
  Suggested Players: +3 Coop Players, +2 Amon Players
  Description: <Map Description> ALL RACES COOP

Battle.Net Info:
 General:
  Website: https://discord.gg/2RbcjRkddw

Game Variants:
 Game Type:
   Team 1/Custom Team Name: Allied Commanders
   Team 2/Custom Team Name: Amon
   Team 3/Custom Team Name: AI

  
  
Terrain:
 Clear Zone 1: remove resources for Player 2/3 , Amon 3, Spawns for 2/3 Players Modes
 Clear Zone 2: remove resources for Player 3, Amon 3, Spawns for 1/3 Players Modes
 Clear Zone 3: remove Spawns for 1/2 Players Modes
 Expansion Area: Expansion resources/ Expansion Rocks for all pplayers
 Initial Exploration:
 Performance Sleep Area:
 Ignore Area:
 Safety Zone: mutator safety zone for All Players modes
 Safety Zone 1: mutator safety zone for 1 Players modes
 Safety Zone 2: mutator safety zone for 2 Players modes
 Safety Zone 3: mutator safety zone for 3 Players modes
 Rebuild Zone Brutal:
 
 
 ZeratulArtifactOrigin ??

Up To 5 Allied Commanders
Up To 2 Amon Players
Amon Bases/Expansions/Mutator Safety Areas


return false if player 16


 Loading Screen:
  Text/Boody:
-------------------------------------------------------
All Races Coop:
- About 50 [ARC] Missions in the Arcade
- ALL RACES COOP Launcher in the Campaigns

All Races PVP:
- ALL RACES PVP Game Extension
- Keiron/Genetron/Xayid/UED/Hybrids/Dragons Races
- Monobattle mode
- Additional game options 

All Races COOP/PVP: https://discord.gg/2RbcjRkddw
Scion Custom Races: https://discord.gg/cSdYbDxEJy
Network Hybrids Race: https://discord.gg/ezMd4GkGkX
UED Race: https://discord.gg/uXcGAz5B
Maguro Mutators: https://www.maguro.one

Thanks To 
RTC2017 contest participants for great maps
Alex007 for inspiration
SC2Mapster community 
-------------------------------------------------------
