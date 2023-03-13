
## Uj projekt létrehozása

[Itt ](https://learn.microsoft.com/en-us/visualstudio/ide/create-csharp-winform-visual-studio?toc=%2Fvisualstudio%2Fget-started%2Fcsharp%2Ftoc.json&bc=%2Fvisualstudio%2Fget-started%2Fcsharp%2Fbreadcrumb%2Ftoc.json&view=vs-2022) 
találtok részletes leírást hogyan tudtok létrehozni egy új Windows Forms alkalmazást, valamint nehány példát hogyan tudjátok az alkalmazást különböző elemekkel ellátni(gombok, bemeneti mezők stb.) 


### Adatbazis kapcsolat letrehozasa
Az adatbázis kapcsolatot az ADO.NET osztályai segíségével hozhatjuk létre. Az ADO.NET szerepe, hogy egy absztrakciós szintet biztosítson a különböző adatforrások(állományok, adatbázisok, web szolgaltatasok stb.) egységes kezelésére

![ADO.net](img/adonet.png)

[Itt találtok több példát, viszont csak a System.Data.SqlClient névtérben található SqlConnection-t adatforrást kell használnunk az alkamazásunk esetén.](https://learn.microsoft.com/en-us/dotnet/framework/data/adonet/ado-net-code-examples#sqlclient )



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


## Egyeb tipusu desktop kliens fejlesztes

### Windows platformra
Ha szeretnetek modernebb felhasznaloi feluletet kesziteni, lehetoseg van egyeb keretrendeszer hasznalatara is: 
- [Universal Windows Platform+WinUI2](https://learn.microsoft.com/en-us/windows/uwp/) az egyik ami ad erre lehetoseget barmilyen Windows eszkozre(PC, Xbox stb). A Microsoft dokumentacioban/githubon talaltok tobb reszletes peldaalkalmazast: 
	[egyszerubbet adatbazis kezelessel](https://learn.microsoft.com/en-us/windows/uwp/enterprise/customer-database-tutorial) vagy [bonyolultabbat de reszletesebbet jo praktikakkal](https://github.com/microsoft/InventorySample) 
	es [van pelda adatbazis kapcsolat letrehozasara is](https://learn.microsoft.com/en-us/windows/uwp/data-access/sql-server-databases).
- [Windows App SDK+ WinUI3](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/) A legujjabb de erre is talalhattok [peldaprojektet](https://github.com/Microsoft/Windows-appsample-customers-orders-database) valamint leirast az [adatbazis kapcsolat letrehozasara ](https://learn.microsoft.com/en-us/windows/apps/develop/data-access/sql-server-database

*Ami fontos hogy ORM keretrendszerek hasznalata nem elfogadott (pl Entity Framework).*

### Linux/Mac 
Hasznalhatto Java ebben az esetben, mivel megtalalhatoak a megfelelo grafikus felhasznaloi komponensek(gombok,listak stb) viszont ORM keretrendszerek(pl. Hibernate) hasznalata nem elfogadott(itt sem).  
Mac-re lehetoseg van Xamarin keretrendszeren keresztuli fejlesztesre viszont [kevesebb peldaprogram erheto el](https://learn.microsoft.com/en-us/xamarin/mac/app-fundamentals/databases)