# projekt-hotovo

Dobrý den, posílám již hotový projekt z MPS na 2.pololetí. Bohužel jsem nemohl pokračovat v rozpracovaném projektu z 1.pololetí jelikož jsem v projektu viděl spoustu nejasností v aplikaci Unity a rpzhodl jsem se že začnu znovu a lépe. Tudíž jsem již měl o mnoho více zkušeností a mohl jsem pracovat více samostatně, jistěji a rychleji. 2D Hru jsem znovu tvořil v Unity a programoval ve Visual Studio Code. S programováním ve visual studiu mám už mnoho zkušeností ze školy z 2. ročníku takže zákládní kódy pro mě nebyly problém. Inspiraci a všechny soubory jsem si stáhl z této série videí: https://youtube.com/playlist?list=PLGmYIROty-5YPWeXeVnQvR9KbMIrL5cM-&si=r225FQSHC2LrRHTR po zhlédnutí této série se mi videa zdály velmi pěkně zpracované a srozumitelné.

Po založení projektu v Unity jsem si založil dvě složky s názvem Scény a Sprites do složky Scény jsem si založil první scénu s názvem Level 1 a do složky Sprites jsem si stáhl všechny soubory a objekty které byli v souboru pod výše uvedeným videem.

Jako první jsem si na pracovní plochu přetáhl soubor s pozadím a nastavil jsem mu šířku 1000, tak aby mezi přechody z levelu do dalšího levelu nebyli místa bez pozadí.
Dále jsem začal pokládat platformy na které bude hráč v levelu skákat a následně jsem přidal také hráče. Nejdřív jsem ale musel natavit na pozadí funkci aby bylo pozadí vždy nastaveno jako poslední vrstva, tak aby se platformy a hráč nepřekrývaly s pozadím. A pak jsem začal level designovat tak aby vypadal dobře, ale hlavně tak aby bylo možné skočit z platformy na další platformu.

Na hráče a na platfromy,stromy,boxy (na to na co hráč bude stoupat) jsem musel přidat komponent s názvem Box Collider 2D který umožnuje to aby hráč nepropadl do země, ale aby zůstal na plošině. Na hráče jsem musel přidat ještě jeden komponent a to s názvem Rigidbody 2D aby měl hráč tzv. "fyzické tělo".
