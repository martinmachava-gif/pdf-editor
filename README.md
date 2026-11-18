# PDF editor

Program pre Windows na úpravu PDF súborov. Beží lokálne, súbory nikam neodosiela
(kvôli licencii sa raz za týždeň spojí s licenčným serverom – posiela len kód počítača, licenčný kľúč a verziu).

**Stiahnutie:** [PdfEditor.exe z poslednej verzie](https://github.com/martinmachava-gif/pdf-editor/releases/latest/download/PdfEditor.exe)
(všetky verzie sú v časti [Releases](https://github.com/martinmachava-gif/pdf-editor/releases)).
Je to jeden súbor pre Windows 10/11 (64-bit), netreba nič inštalovať. Pri prvom spustení môže Windows ukázať
„Systém Windows ochránil váš počítač“ – program nie je digitálne podpísaný, stačí *Ďalšie informácie → Spustiť aj tak*.

## Čo vie

- otvoriť PDF (aj chránené heslom), listovať, približovať (Ctrl + koliesko)
- strany v paneli vľavo: presúvanie ťahaním, otáčanie, duplikovanie, mazanie, prázdna strana,
  vloženie iného PDF (aj pretiahnutím do panela), uloženie vybraných strán ako nové PDF, rozdelenie na jednotlivé strany
- **upraviť pôvodný text**: nástroj *Upraviť text*, klik na riadok v PDF a prepísanie; písmo, veľkosť a farba sa
  nastavia podľa pôvodného, starý text sa pri uložení z PDF odstráni (ak sa to na strane nedá bezpečne, len sa prekryje)
- pridať text s diakritikou v ľubovoľnom písme nainštalovanom vo Windows (veľkosť, farba, tučné, kurzíva), pero, zvýrazňovač, obdĺžnik, čiaru, šípku
- biele zakrytie (prekryje obsah) a začiernenie (pri uložení obsah naozaj odstráni – strana sa uloží ako obrázok)
- obrázok (pečiatka, logo) a podpis (nakreslený myšou alebo z obrázka, dá sa zapamätať)
- **zamknutie heslom**: Súbor → Zabezpečenie – heslo na otvorenie (šifrovanie AES-256) a obmedzenia tlače, úprav
  a kopírovania; súbor, ktorý už heslo mal, si ho pri uložení ponechá
- **označenie a kopírovanie textu**: nástrojom Výber potiahnuť cez text a Ctrl+C; pravým tlačidlom zvýrazniť,
  podčiarknuť alebo prečiarknuť
- **skeny**: text v naskenovaných stranách sa rozpozná automaticky (rozpoznávanie textu vo Windows, slovenčina);
  potom sa dá označiť, kopírovať aj prepísať nástrojom Upraviť text a uložené PDF je prehľadávateľné
- **skenovanie** priamo zo skenera (cez Windows aj ovládač výrobcu TWAIN) a **PDF z obrázkov a fotiek**
- **hľadanie** (Ctrl+F) bez ohľadu na diakritiku, **zmenšenie PDF** na e-mail, **pečiatky** s dátumom
- **číslovanie strán, hlavička, päta, vodoznak**, uloženie strán ako obrázky, klikateľné odkazy, **obsah (záložky)**
- **obnova po páde** a **automatická aktualizácia** z GitHubu (Pomoc → Skontrolovať aktualizácie)
- vypĺňanie PDF formulárov (textové polia, zaškrtávacie políčka, výberové zoznamy) a **vytváranie nových polí**
  (Formulár → Textové pole / Zaškrtávacie pole / Rozbaľovací zoznam)
- **karty** pre viac otvorených PDF naraz; PDF otvorené z Prieskumníka sa otvorí ako nová karta v bežiacom okne
- **orezanie strán** (ťahom myši, orezanie bielych okrajov, rovnaké orezanie ďalších strán)
- **poznámky** (komentáre), ktoré vidí aj Acrobat či Edge; karta *Poznámky* so zoznamom
- **elektronický podpis** certifikátom z Windows (eID karta s eID klientom, iná čipová karta) alebo zo súboru .pfx –
  formát PAdES; pri otvorení editor overí, či sa podpísaný dokument nezmenil
- Späť / Znova, kopírovanie objektov medzi stranami (Ctrl+C / Ctrl+V), tlač
- Pomoc → *Otvárať PDF súbory týmto editorom* pridá editor do ponuky „Otvoriť pomocou“
- **licencia**: 14 dní zadarmo plná verzia, potom s licenčným kľúčom (Pomoc → Licencia);
  bez licencie ostáva prezeranie, hľadanie, kopírovanie textu a tlač

## Čo nevie

- preformátovať celý odsek (úprava ide po riadkoch, text sa nezalamuje do ďalšieho riadku)
- použiť presne pôvodné písmo, ak nie je nainštalované vo Windows (použije sa najpodobnejšie);
  písma typu OpenType/CFF (.otf) a písma, ktorých licencia nepovoľuje vkladanie do PDF, sa neponúkajú
- presne prepísať text v skene: starý text sa prekryje farbou papiera a nový sa napíše podobným písmom;
  pri pečiatkach, rukopise a drobnom písme sa rozpoznávanie môže pomýliť

## Licencia a použité knižnice

Od verzie 1.5.0 program potrebuje licenciu. Po prvom spustení ponúkne **14 dní zadarmo** plnú verziu
(raz na počítač, treba internet). Potom sa zadá **licenčný kľúč** v okne Pomoc → Licencia; licencia platí
na počítači, kde bola aktivovaná, a dá sa preniesť na iný (Deaktivovať na tomto počítači). Počítač bez internetu
sa dá aktivovať ručne kódom poslaným e-mailom. Bez licencie môžete PDF ďalej prezerať, hľadať v nich,
kopírovať text a tlačiť.

Zdrojový kód programu nie je verejný. Všetky práva vyhradené.

Program používa tieto knižnice tretích strán:
- [PDFium](https://pdfium.googlesource.com/pdfium/) – © The PDFium Authors, licencia BSD 3-Clause a Apache 2.0
  (zostavenie [pdfium-binaries](https://github.com/bblanchon/pdfium-binaries))
- [PDFsharp](https://github.com/empira/PDFsharp) 6.2 – © empira Software GmbH, licencia MIT
- [.NET](https://dotnet.microsoft.com/) – © Microsoft, licencia MIT
