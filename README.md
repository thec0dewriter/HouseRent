
## Uj projekt létrehozása

[Itt ](https://learn.microsoft.com/en-us/visualstudio/ide/create-csharp-winform-visual-studio?toc=%2Fvisualstudio%2Fget-started%2Fcsharp%2Ftoc.json&bc=%2Fvisualstudio%2Fget-started%2Fcsharp%2Fbreadcrumb%2Ftoc.json&view=vs-2022) 
találtok részletes leírást hogyan tudtok létrehozni egy új Windows Forms alkalmazást, valamint nehány példát hogyan tudjátok az alkalmazást különböző elemekkel ellátni(gombok, bemeneti mezők stb.) 


### Adatbazis kapcsolat letrehozasa
Az adatbázis kapcsolatot az ADO.NET osztályai segíségével hozhatjuk létre. Az ADO.NET szerepe, hogy egy absztrakciós szintet biztosítson a különböző adatforrások(állományok, adatbázisok, web szolgaltatasok stb.) egységes kezelésére

![ADO.net](img/adonet.png)

[Itt találtok több példát, viszont csak a SQL adatforrást kell használnunk az alkamazásunk esetén.](https://learn.microsoft.com/en-us/dotnet/framework/data/adonet/ado-net-code-examples )

## Példa projekt importálásának lépései

### 1.lépés
nyaralo_script.sql végrehajtása (létrejön az adatbázis s annak táblái és feltöltodnek adatokkal)

### 2. lépés
  Példa projekt megnyitása Visual Studio-val. 
  Ez torténhet .sln(solution) kiterjesztesű állomány megnyitásával vagy a Visual  Studio `File->Open` opciojával.

### 3.lépés
DALGen.cs fájlban a kapcsolati karakterlánc (strSqlConn) testreszabása. Ebben az allomanyban találtok példát és némi magyarázatot, hogy hogyan dolgozz az ADO.NET.


### 4.lépés
Program futtatása : Start

