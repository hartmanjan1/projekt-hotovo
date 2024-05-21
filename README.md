# projekt-hotovo

Dobrý den, posílám již hotový projekt z MPS na 2.pololetí. Bohužel jsem nemohl pokračovat v rozpracovaném projektu z 1.pololetí jelikož jsem v projektu viděl spoustu nejasností v aplikaci Unity a rpzhodl jsem se že začnu znovu a lépe. Tudíž jsem již měl o mnoho více zkušeností a mohl jsem pracovat více samostatně, jistěji a rychleji. 2D Hru jsem znovu tvořil v Unity a programoval ve Visual Studio Code. S programováním ve visual studiu mám už mnoho zkušeností ze školy z 2. ročníku takže zákládní kódy pro mě nebyly problém. Inspiraci a všechny soubory jsem si stáhl z této série videí: https://youtube.com/playlist?list=PLGmYIROty-5YPWeXeVnQvR9KbMIrL5cM-&si=r225FQSHC2LrRHTR po zhlédnutí této série se mi videa zdály velmi pěkně zpracované a srozumitelné.

Po založení projektu v Unity jsem si založil dvě složky s názvem Scény a Sprites do složky Scény jsem si založil první scénu s názvem Level 1 a do složky Sprites jsem si stáhl všechny soubory a objekty které byli v souboru pod výše uvedeným videem.

Jako první jsem si na pracovní plochu přetáhl soubor s pozadím a nastavil jsem mu šířku 1000, tak aby mezi přechody z levelu do dalšího levelu nebyli místa bez pozadí.
Dále jsem začal pokládat platformy na které bude hráč v levelu skákat a následně jsem přidal také hráče. Nejdřív jsem ale musel natavit na pozadí funkci aby bylo pozadí vždy nastaveno jako poslední vrstva, tak aby se platformy a hráč nepřekrývaly s pozadím. A pak jsem začal level designovat tak aby vypadal dobře, ale hlavně tak aby bylo možné skočit z platformy na další platformu.

Na hráče a na platfromy,stromy,boxy (na to na co hráč bude stoupat) jsem musel přidat komponent s názvem Box Collider 2D který umožnuje to aby hráč nepropadl do země, ale aby zůstal na plošině. Na hráče jsem musel přidat ještě jeden komponent a to s názvem Rigidbody 2D aby měl hráč tzv. "fyzické tělo".


Dále jsem se rozhodl přidat fyzické materiály na které jsem si založil vlastní složku v Unity. Přidal jsem 2 fyzické materiály jménem Bouncy a Slippery (skákání a klouzání) Bouncy jsem přidal na objekt hráče a Slippery jsem přidal na boxy které jsem chtěl aby se hýbaly při stoupnutí hráče na ně.

Přidal jsem také dlaždice které jsem umístil na okraj mapy tak aby levely vypadaly lépe. Na dlaždice jsem nepřidal žádné komponenty jelikož nepotřebuji aby na ně hráč padal. Jelikož tam jsou jen na design, tak aby levely vypadaly lépe.

Po přidání dlaždic jsem si soubory uspořadal do složek, tak aby se mi s nimi do budoucna lépe pracovalo.
Teď už přišli na řadu Scripty takže jsem si založil novou složku s názvem Scripty kde jsem založil nový C#script a dal mu název Ovládání. Otevřel jsem Visual Studio a do scriptu jsem mohl začít psát. Jako první jsem chtěl přidat pohyb hráče doleva,doprava a skok. Klávesy jsem pro pohyb nastavil A a D a pro výskok mezerník. Pohyb hráče jsem přidal tímto příkazem:
