## Installation
- In all ```include```
```pawn
#define USE_CUSTOM_FUEL_FOR_CAMPER //If you need to add fuel to the camper
#include <camper>
```

- In ```OnGameModeInit``` after connecting to the database
```pawn
camper_InitMysqlHandle(/*connection variable*/); //For example, dbHandle
```


- At the very end of ```OnPlayerSpawn```, add:
```pawn
OnPlayerSpawnCamper(playerid);
```


- At the end of the mod
```pawn
//Fuel
stock SetCamperFuel(vehicleid)
{
    VehicleInfo[vehicleid] = 100; // Replace VehicleInfo with your own array where fuel is stored
}

// Money
stock camper_GetPlayerMoney(playerid)
{
    return PlayerInfo[playerid][pMoney]; // Replace PlayerInfo[playerid][pMoney] with your own
}

stock camper_SetPlayerMoney(playerid, cmp_money)
{
    PlayerInfo[playerid][pMoney] += cmp_money; //Replace PlayerInfo[playerid][pMoney] with your own
}

//Materials
stock camper_GetPlayerMats(playerid)
{
    return PlayerInfo[playerid][pMats]; //Replace PlayerInfo[playerid][pMats] with your own
}

stock camper_SetPlayerMats(playerid, cmp_mats)
{
    PlayerInfo[playerid][pMats] += cmp_mats; //Replace PlayerInfo[playerid][pMats] with your own
}

//Drugs
stock camper_GetPlayerDrugs(playerid)
{
    return PlayerInfo[playerid][pDrugs]; //PlayerInfo[playerid][pDrugs] Replace with your own
}

stock camper_SetPlayerDrugs(playerid, cmp_drugs)
{
    PlayerInfo[playerid][pDrugs] += cmp_drugs; //PlayerInfo[playerid][pDrugs] Replace with your own
}
```


Translated with DeepL.com (free version)
