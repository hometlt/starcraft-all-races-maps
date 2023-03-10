
([^\d\w.])([345])([^\d.])
$1gv_pLAYER_0$2_ENEMY$3


libNtve_gf_CreateUnitsWithDefaultFacing\((\d+), "(\w+)", 0, 3
libNtve_gf_CreateUnitsWithDefaultFacing\($1, "$2", 0, gv_pLAYER_03_ENEMY

libNtve_gf_CreateUnitsWithDefaultFacing\((\d+), "(\w+)", 0, 4
libNtve_gf_CreateUnitsWithDefaultFacing\($1, "$2", 0, gv_pLAYER_04_ENEMY

libNtve_gf_CreateUnitsWithDefaultFacing\((\d+), "(\w+)", 0, 5
libNtve_gf_CreateUnitsWithDefaultFacing\($1, "$2", 0, gv_pLAYER_05_ALLY


(UnitCreate\([^,]*,[^,]*,[^,]*, )([3|4|5]),
$1XXPLAYER$2,

(AINearestTownBullyRebuild\()([3|4|5]),
$1XXPLAYER$2,



UnitGetOwner
AICampaignStart
AIToggleBulliesInRegion()
libNtve_gf_SetUpgradeLevelForPlayer()
AISetBullyRebuildDelay(,,3);
libNtve_gf_ShareVisionofUnit(,,3);
AISetBullyRebuildDelay(,,4);
    
    
    
    
    
TriggerAddEventTimeElapsed(gt_Convoy3Spawn2, 1050.0, c_timeGame);
TriggerAddEventTimePeriodic(gt_Convoy3Spawn2, 1050.0, c_timeGame);

c_timeAI


//--------------------------------------------------------------------------------------------------
// Global Variables
//--------------------------------------------------------------------------------------------------
...
timer gv_specialTriggerTimer;

...

void InitGlobals () {
    gv_specialTriggerTimer = TimerCreate();
    
...
    
bool gt_StartGameQ_Func (bool testConds, bool runActions) {
    TimerStart(gv_specialTriggerTimer, lp_time, false, c_timeGame);
            
...
            
TriggerAddEventTimer(gt_Trigger, gv_specialTriggerTimer);



//--------------------------------------------------------------------------------------------------
// Constants
//--------------------------------------------------------------------------------------------------
int gv_pLAYER_01_USER = 1;
int gv_pLAYER_02_USER = 2;

bool gt_Init02Players_Func (bool testConds, bool runActions) {
...
    gv_pLAYER_01_USER = libCOMI_gf_GetRolePlayer(1);
    gv_pLAYER_02_USER = libCOMI_gf_GetRolePlayer(2);
    
    
    
    
    
    AIAttackWaveSetTargetPlayer(gv_pLAYER_05_ALLY, lv_amonSupportGroup);
    AIAttackWaveSetTargetPlayer(gv_pLAYER_06_HYBRID, PlayerGroupSingle(gv_pLAYER_05_ALLY));
