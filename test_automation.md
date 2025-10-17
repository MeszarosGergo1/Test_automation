# Tesztautomatizálási kérdések

## Tesztelési alapok (ISTQB-hez kapcsolódó)
<img src="https://www.mindsmapped.com/wp-content/uploads/2016/06/ISTQB.jpg" alt="image" width="300" height="220">

## A tesztelés alapjai:
#### Mi a tesztelés célja? Mi nem az?
    Célja a hibák feltárása a szoftverben, és annak bebizonyítása, hogy a rendszer nem hibamentes.
    A tesztelés célja nem a hibák hiányának bizonyítása, hanem annak kimutatása, hogy vannak benne problémák.

#### Mi a kapcsolat a tesztelés és a hibamegelőzés között?
    A korai és rendszeres tesztelés hozzájárul a hibák megelőzéséhez.
    Ha a tesztelés már a követelmények és a tervezés szintjén elindul, akkor a problémákat hamarabb és olcsóbban lehet elhárítani.
    A hibamegelőzés célja tehát nemcsak a hibák feltárása, hanem azok megelőzése a fejlesztési folyamat korai szakaszában.

#### Miért fontos, hogy a tesztelők függetlenek legyenek a fejlesztőktől?
    A függetlenség segít objektíven értékelni a szoftvert.
    A fejlesztők hajlamosak elnézni saját hibáikat vagy nem észrevenni őket, mert ismerik a rendszer működését.
    A független tesztelők ezzel szemben friss szemmel, elfogulatlanul vizsgálják a programot, és olyan problémákat is megtalálhatnak, amelyeket a fejlesztők nem vennének észre.

#### Mi a veszélye annak, ha a fejlesztő maga teszteli a saját kódját?
    A fejlesztő nem mindig tudja objektíven megítélni a saját munkáját, és hajlamos feltételezni, hogy a kódja helyesen működik.
    Ezért előfordulhat, hogy a tesztelés nem fedezi fel a valós hibákat.
    Ez a fajta önellenőrzés növeli annak kockázatát, hogy a hibák rejtve maradnak a fejlesztési folyamat későbbi szakaszáig.

#### Mik a tesztelési alapelvek?
    1. A kimerítő tesztelés lehetetlen – nem tesztelhető minden lehetséges bemenet és feltétel.
    2. A hibák halmozódnak – a hibák többsége kevés számú modulban koncentrálódik (Pareto-elv: 80/20).
    3. A peszticid-paradoxon – ha mindig ugyanazokat a teszteket futtatjuk, egy idő után már nem találunk új hibákat.
    4. A tesztelés hibákat mutat ki, nem a hibátlanságot bizonyítja – a cél a hibák feltárása, nem az igazolás, hogy a szoftver tökéletes.
    5. A hibák hiánya nem jelenti, hogy a rendszer használható – lehet, hogy a szoftver hibamentes, de nem felel meg az üzleti céloknak.
    6. A korai tesztelés fontos – a hibák feltárása a fejlesztés korai szakaszában sokkal olcsóbb és hatékonyabb.
    7. A tesztelés kontextustól függ – különböző rendszerek különböző tesztelési megközelítést igényelnek (pl. webáruház ≠ beágyazott rendszer).

#### Mit jelent az „alapvető tesztelési elv”, hogy „a kimerítő tesztelés lehetetlen”?
    Nem lehetséges minden egyes bemenetet, kombinációt és állapotot tesztelni.
    Még egy egyszerű űrlap vagy fájlművelet esetén is végtelen számú lehetséges teszteset lenne.
    Ezért a tesztelésnek prioritásokat kell felállítania, és a kockázatelemzés alapján kell kiválasztania az optimális teszteseteket.

#### Mit jelent az „alapvető tesztelési elv”, hogy „a hibák halmozódnak”?
    A hibák általában néhány modulban koncentrálódnak, nem egyenletesen oszlanak el a rendszerben.
    Ezt a Pareto-elv is leírja: a hibák 80%-a a kód 20%-ában található.
    A tapasztalat segít felismerni ezeket a kritikus területeket, így a tesztelés során ezekre kell összpontosítani.

#### Mit jelent az „alapvető tesztelési elv”, hogy „a tesztelés a kontextustól függ”?
    A tesztelési módszer és stratégia mindig a szoftver típusától és céljától függ.
    Másképp kell tesztelni például egy pénzügyi rendszert, ahol az adatpontosság a legfontosabb, és máshogy kell tesztelni, mint egy webáruházat, ahol a felhasználói élmény a kulcs.
    A tesztelési megközelítés tehát mindig a kontextushoz igazodik, nincs univerzális módszer minden szoftverhez.


## 2. Tesztelés a szoftverfejlesztés életciklusán át
#### Mik a tesztszintek, és mi a különbség köztük?
    A tesztszintek a szoftverfejlesztés különböző fázisaihoz kapcsolódnak.
    Az egységteszt (unit test) egyetlen modul vagy komponens tesztelésére szolgál.
    Az integrációs teszt az egyes modulok együttműködését ellenőrzi.
    A rendszerteszt az egész alkalmazás funkcióit vizsgálja a specifikációk szerint.
    A felhasználói elfogadási teszt (UAT) során a végfelhasználó ellenőrzi, hogy az alkalmazás megfelel-e az üzleti igényeknek.

#### Miért nem érdemes mindig ugyanazokat a teszteseteket futtatni (regressziós torzítás)?
    Az ismétlődő tesztek nem fedeznek fel új hibákat, ami a Pesticide Paradox jelensége.
    Ezért a tesztkészletet rendszeresen frissíteni és bővíteni kell, hogy új problémák is észrevehetők legyenek.

#### Mi az egységtesztelés (unit testing)? Ki felelős az egységtesztek írásáért?
    Az egységtesztelés során a szoftver legkisebb egységeit, például funkciókat vagy modulokat külön tesztelnek.
    Általában a fejlesztő írja az egységteszteket, mert ő ismeri a kód részleteit a legjobban.

#### Mi a különbség a verifikáció és a validáció között?
    A verifikáció azt ellenőrzi, hogy a szoftver megfelel-e a specifikációknak („megfelelően készült-e”), míg a validáció azt ellenőrzi, hogy a szoftver megfelel-e a felhasználói és üzleti igényeknek („megfelel-e a valós célokra”).

#### Mik a tesztelési típusok, és mi a különbség köztük?
    A funkcionális teszt a szoftver funkcióit ellenőrzi a specifikáció alapján, míg a nem-funkcionális teszt a teljesítményt, biztonságot, használhatóságot vagy kompatibilitást vizsgálja.

#### Mi a különbség a fehér doboz, szürke doboz és fekete doboz tesztelés között?
    A fehér doboz tesztelés a kód és logika teljes ismeretét igényli.
    A fekete doboz tesztelés csak a bemenetek és kimenetek alapján történik, a belső logikát nem ismeri.
    A szürke doboz tesztelés részleges belső információval dolgozik, például modulkapcsolatok vagy adatfolyamok ismeretével.

#### Mi a különbség a felhasználói elfogadási teszt (UAT) és a rendszerteszt között?
    A rendszertesztet szakmai csapat végzi, hogy ellenőrizze az egész rendszer működését a specifikációk szerint.
    A felhasználói elfogadási tesztet a végfelhasználó végzi, hogy biztosítsa a szoftver használhatóságát és az üzleti célok teljesülését.

#### Mi a különbség a statikus és dinamikus tesztelés között?
    A statikus tesztelés során a kódot vagy dokumentációt elemzik futtatás nélkül, például kód review vagy statikus analízis formájában.
    A dinamikus tesztelés során a szoftvert ténylegesen futtatják, és ellenőrzik a viselkedését a különböző bemenetekre.