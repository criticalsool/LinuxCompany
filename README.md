<img src="https://lethalcompany.net/wp-content/uploads/2023/12/Lethal-Company-Logo-300x225.png" alt="drawing" width="100"/>

# LinuxCompany
Make LethalCompany working on Linux, specially with mods

## Install BepInEx
Go to [Thundertore/BepInEx](https://thunderstore.io/c/lethal-company/p/BepInEx/BepInExPack/) and clic on `Manual Download`.

- Open your game folder like this :
<img src="https://github.com/criticalsool/LinuxCompany/assets/164774099/86792c23-6a50-495c-af65-51ffd6d81b9b" alt="image" style="width:400px;height:auto;">

- Copy the content of the archive in the game folder like this :
<img src="https://github.com/criticalsool/LinuxCompany/assets/164774099/0a7b8322-2a19-49e5-b2b0-39a4dc70547a" alt="image" style="width:500px;height:auto;">

- Add steam launch options
```bash
WINEDLLOVERRIDES="winhttp.dll=n,b"
```

- Launch the game

## Install mods
- Quit the game
- Manually download mods here : [Thunderstore/LethalCompany](https://thunderstore.io/c/lethal-company)
- Copy the contents in the `plugins` folder
<img src="https://github.com/criticalsool/LinuxCompany/assets/164774099/6ba5ee94-21fc-4191-863a-35e81226d950" alt="image" style="width:600px;height:auto;">

- Steam launch options

Add your mod `dll` (like `HDLethalCompany.dll`) in the `WINEDLLOVERRIDES`, seperated by commas like this :

```bash
WINEDLLOVERRIDES="winhttp.dll,<YOUR_MODS_DLL>,HDLethalCompany.dll=n,b"
```

If you are on Linux, you can generate this list with this command in the plugins folder :
```bash
ls -R | grep -E "*.dll" | sed -z "s/\n/,/g"
```

My launch option as an example
```bash
WINEDLLOVERRIDES="winhttp.dll,AlwaysHearWalkie.dll,BetterStamina.dll,EladsHUD.dll,FovAdjust.dll,HDLethalCompany.dll,HideChat.dll,HornMoan.dll,LateCompanyV1.0.12.dll,LCBetterSaves.dll,LetMeLookDown.dll,MaskedEnemyRework.dll,Mimics.dll,MoreBlood.dll,MoreCompany.dll,MoreEmotes1.3.3.dll,MoreSuits.dll,NameplateTweaks.dll,NicholaScott.BepInEx.RuntimeNetcodeRPCValidator.dll,Peepers.dll,QuickRestart.dll,Scopophobia.dll,SkinwalkerMod.dll,SpectateEnemy.dll,TerminalApi.dll,TerminalClock.dll,LethalCompanyInputUtils.dll,LethalLib.dll,ShipLoot.dll=n,b" gamemoderun %command%
```

- Enjoy !

> Credits : [LethalCompany](https://lethalcompany.net), [BepInEx](https://github.com/BepInEx/BepInEx), [Thunderstore](https://thunderstore.io/c/lethal-company), 
