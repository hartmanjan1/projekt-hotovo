# projekt-hotovo

Dobrý den, posílám již hotový projekt z MPS na 2.pololetí. Bohužel jsem nemohl pokračovat v rozpracovaném projektu z 1.pololetí jelikož jsem v projektu viděl spoustu nejasností v aplikaci Unity a rozhodl jsem se že začnu znovu a lépe. Tudíž jsem již měl o mnoho více zkušeností a mohl jsem pracovat více samostatně, jistěji a rychleji. 2D Hru jsem znovu tvořil v Unity a programoval ve Visual Studio Code. S programováním ve visual studiu mám už mnoho zkušeností ze školy z 2. ročníku takže zákládní kódy pro mě nebyly problém. Inspiraci a všechny soubory jsem si stáhl z této série videí: https://youtube.com/playlist?list=PLGmYIROty-5YPWeXeVnQvR9KbMIrL5cM-&si=r225FQSHC2LrRHTR po zhlédnutí této série se mi videa zdály velmi pěkně zpracované a srozumitelné.

Po založení projektu v Unity jsem si založil dvě složky s názvem Scény a Sprites do složky Scény jsem si založil první scénu s názvem Level 1 a do složky Sprites jsem si stáhl všechny soubory a objekty které byly v souboru pod výše uvedeným videem.

Jako první jsem si na pracovní plochu přetáhl soubor s pozadím a nastavil jsem mu šířku 2000, tak aby mezi přechody z levelu do dalšího levelu nebyli místa bez pozadí.
Dále jsem začal pokládat platformy na které bude hráč v levelu skákat a následně jsem přidal také hráče. Nejdřív jsem ale musel natavit na pozadí funkci aby bylo pozadí vždy nastaveno jako poslední vrstva, tak aby se platformy a hráč nepřekrývaly s pozadím. A pak jsem začal level designovat tak aby vypadal dobře, ale hlavně tak aby bylo možné skočit z platformy na další platformu.

Na hráče a na platfromy, stromy ,boxy (na to na co hráč bude stoupat) jsem musel přidat komponent s názvem Box Collider 2D který umožnuje to aby hráč nepropadl do země, ale aby zůstal na plošině. Na hráče jsem musel přidat ještě jeden komponent a to s názvem Rigidbody 2D aby měl hráč tzv. "fyzické tělo".


Dále jsem se rozhodl přidat fyzické materiály na které jsem si založil vlastní složku v Unity. Přidal jsem 2 fyzické materiály jménem Bouncy a Slippery (skákání a klouzání) Slippery jsem přidal na boxy které jsem chtěl aby se hýbaly při stoupnutí hráče na ně.

Přidal jsem také dlaždice které jsem umístil na okraj mapy tak aby levely vypadaly lépe. Na dlaždice jsem nepřidal žádné komponenty jelikož nepotřebuji aby na ně hráč padal. Jelikož tam jsou jen na design, tak aby levely vypadaly lépe.

Po přidání dlaždic jsem si soubory uspořadal do složek, tak aby se mi s nimi do budoucna lépe pracovalo.
Teď už přišli na řadu Scripty takže jsem si založil novou složku s názvem Scripty kde jsem založil nový C#script a dal mu název Ovládání. Otevřel jsem Visual Studio a do scriptu jsem mohl začít psát. Jako první jsem chtěl přidat pohyb hráče doleva, doprava a skok. Klávesy jsem pro pohyb nastavil A a D a pro výskok mezerník. Pohyb hráče jsem přidal tímto příkazem:

![1](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/48f3134f-d601-49cb-93f5-57c92e36e365)

![2](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/ef1b9e16-dbb1-49bc-ae02-ed6cdc2c3aa8)

Teď se mi již hráč pohyboval do stran a mohl vyskočit, ale často se mi stávalo že se hráč o platformu na kterou skáče "zasekne", a tak jsem musel na každou jednotlivou platformu přidat fyzický materiál jménem Slippery který jsem si již v minulosti vytvořil.
Hráč má momentálně nekonečno výskoků,  ale mým cílem je aby mohl skákat pouze když se dotýká platformy nebo boxu s komponentem Collider 2D, proto jsem na každou platformy nebo box musel přidat tzv. GroundCheck a nastavil jsem mu hodnotu 0.2 jelikož můj hráč je velký tak aby mohl mít tuto hodnotu. Groundcheck je příkaz který umožní to že hráč bude moci vyskočit jen jednou.
Použil jsem proto tyhle čtyři příkazy:

![2](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/99480746-d79a-48e0-b553-95cdc3dbc422)

A následně tento delší příkaz: 

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/1db8cb38-a84f-4ae4-b13b-1bc433608532)
![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/bdba37eb-2e6c-4015-9582-4662a6d337d0)

Jelikož jsem již měl přidané vše potřebné tak by hra již fungovala, ale rozhodl jsem se přidat ještě pár věcí.
Jako další jsem chtěl přidat animace. Z minulého pololetního projektu si pamatuji že animace pro mně byly jeden z největších problémů takže jsem se rozhodl pokračovat spíše podle videa než podle sebe.
Začal jsem tak že jsem si stáhl všechny jednotlivé snímky hráče a přetáhl je na časovou osu kde jsem si je uspořádal tak jak jdou za sebou ve stejných intervalech. Animoval jsem převážně jen hráče a pak jednu platformu tak aby byla pohyblivá. 
![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/9e0c1565-649b-4c0a-b4fc-037aa06f26b5)

U hráče jsem měl hned tři animace - pro chůzi, výskok a když je hráč v normálním, nehybném stavu.
Animaci pro platformu jsem udělal stejně jako animaci na pohyb hráče.

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/b3621219-ef6b-4026-9b5d-3447d83dafe1)

V sekci animator jsem naprogramoval animace tak jak jdou z sebou.
Aby animace plně fungovali musel jsem je ještě naprogramovat ve Visual Studiu těmito jednoduchými kódy: 

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/c72f4c12-44b3-48a5-8f1c-1f2f9e2e3abb)
![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/be8c8f8e-0cb6-41c3-aabc-00ccc79b01fc)
![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/c711b75f-6c95-4ba0-ab25-da934db9f77c)

Teď se již hráč plně i se všemi animacemi pohyboval, ale kamera ho stále nesledovala. Takže mohl ujít jen pár bloků. To jsem změnil tak že jsem založil nový skript jménem CameraController a přetáhl ho na hlavní kameru. Tady jsem uplně vynechal video ze série kterou sleduji a udělal jsem to podobně jak jsem to dělal v prvním pololetí. Do skriptu určeného jen pro kameru jsem napsal tyto příkazi: 

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/660ad16d-b298-4dba-9a39-ef2f3aab3d41)

a pak jen přetáhl do skriptu objekt hráče. To umožnilo to že kamera bude sledovat jen hráče a prostor kolem něho. Takže teď když se hráč rozběhl tak mohl běžet a skákat dál než jen pár bloků.

Jenže když hráč spadl z plošiny dolů tak jsem vždy musel restartovat hru aby se na plošinu zase vrátil. To jsem změnil tak že jsem pod scénu hry vložil po celé délce FallDetector, který funguje jako takový senzor a když ním hráč propadne tak ho vrátí zpět na start.

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/5e6172d5-95f2-4faf-8e3d-e238097d7bff)

Aby FallDetector dobře fungoval tak jsem musel přidat hned několik příkazů: 

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/e5b49539-66c3-4876-9a85-37b12660814e)
![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/cd7b1689-705a-4ad0-a8fe-03e2d19b5d08)

A jelikož je herní scéna poměrně dlouhá rozhodl jsem se do ní přidat hned několik checkpointů, tak aby když hráč spadne nakonci nemusel absolvovat celou mapu znovu.

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/2774e96e-2603-43cb-9df9-b4fb27af942d)

Na checkpointy jsem přidal komponent Box Collider 2D a zaškrtnul políčko is Trigger, tak aby checkpoint zaregistroval pohyb hráče.
Pak už stačilo vložit krátký příkaz:

![image](https://github.com/hartmanjan1/projekt-hotovo/assets/156115281/b650fa4e-cc02-493c-9461-71438e238762) 

Následně jsem na checkpointy přidal soubor portálu aby hráč viděl kdy následuje další checkpoint.

Aby hra byla více zábavná přidal jsem na platformy malé krystaly které musí hráč při hraní hry sbírat.

Pak jsem jenom upravil pohyb a rychlost hráče, tak aby hra vypadala více přirozeně.

Na vybrané boxy jsem přidal fyzický materiál Bouncy a nastavil na hodnotu 0.8 tak aby boxy fungovaly jako trampolína.

A to je vše. Níže přiložím video ze hry. 

Díky této zkušenosti jsem se naučil mnoho příkazů do Visual Studia a naučil jsem se lépe využívat program Unity.
V programování her budu určitě pokračovat.

Děkuji Hartman S3E.











