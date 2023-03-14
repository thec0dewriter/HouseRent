
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
A valid ConnectionString(kapcsolati karakterlanc) letrehozasara hasznalhatjatok a [SqlConnectionStringBuilder](https://learn.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlconnectionstringbuilder?view=dotnet-plat-ext-7.0) osztalyt.

### 4.lépés
Program futtatása : Start


## Projekt strukturalis elrendezes
A pelda projekt a kiindulasi pont a minimalis strukturalis elrendezesre. Fontos hogy az adatbazisra történo kapcsolat letrehozasa, a tablakon valo műveletek és megjelenitési rész megfelelően el legyenek választva.
Erre nehany iranyelv:
- Data Access Layer(DAL): az adatbazis kapcsolat kezelesere
- Repository minta: az tablak kezelesere (sorok hozzaadasa, torlese, lekerdezese)
- MVP/MVC/MVVM: a felhasznaloi feluleten valo megjelenites valamint felhasznalo interakciora.

Nem kötelező az MVP/MVC/MVVM tervezési minta használata, azonban az adatkezelési réteg (Model) és a grafikus felület (View) elkülönítését mindenképp meg kell oldani, vagyis:
A projektben is minden olyan táblára vonatkozóan létre kell hoznunk egy új osztályt,amelyben az adott táblához kapcsolódó konkrét lekérdezéseket írjuk.
A példaprogramok esetén ezek az osztályok a Houses.cs, Countries.cs, Owners.cs. Ezenkívül minden táblára egy-egy adattípus is (struct) létre van hozva: House, Country és Owner.

[(Itt talaltok egy MVP megvalositast, s nehany kodreszletet)](https://www.youtube.com/watch?v=WSBy_Ypgk38&ab_channel=RJCodeAdvanceEN)




## Egyeb tipusu desktop kliens fejlesztes

### Windows platformra
Ha szeretnetek modernebb felhasznaloi feluletet kesziteni, lehetoseg van egyeb keretrendeszer hasznalatara is: 
- [Universal Windows Platform+WinUI2](https://learn.microsoft.com/en-us/windows/uwp/) az egyik ami ad erre lehetoseget barmilyen Windows eszkozre(PC, Xbox stb). A Microsoft dokumentacioban/githubon talaltok tobb reszletes peldaalkalmazast: 
	[egyszerubbet adatbazis kezelessel](https://learn.microsoft.com/en-us/windows/uwp/enterprise/customer-database-tutorial) vagy [bonyolultabbat de reszletesebbet jo praktikakkal](https://github.com/microsoft/InventorySample) 
	es [van pelda adatbazis kapcsolat letrehozasara is](https://learn.microsoft.com/en-us/windows/uwp/data-access/sql-server-databases).
- [Windows App SDK+ WinUI3](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/) A legujjabb de erre is talalhattok [peldaprojektet](https://github.com/Microsoft/Windows-appsample-customers-orders-database) valamint leirast az [adatbazis kapcsolat letrehozasara ](https://learn.microsoft.com/en-us/windows/apps/develop/data-access/sql-server-database

*Ami fontos hogy ORM keretrendszerek (pl Entity Framework) vagy LINQ hasznalata nem elfogadott.*

### Linux/Mac 
Hasznalhatto Java ebben az esetben, mivel megtalalhatoak a megfelelo grafikus felhasznaloi komponensek(gombok,listak stb) viszont ORM keretrendszerek(pl. Hibernate) hasznalata nem elfogadott(itt sem).  
Mac-re lehetoseg van Xamarin keretrendszeren keresztuli fejlesztesre viszont [kevesebb peldaprogram erheto el](https://learn.microsoft.com/en-us/xamarin/mac/app-fundamentals/databases)


