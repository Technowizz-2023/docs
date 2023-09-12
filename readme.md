# Zadání

Původní znění: https://img.beclever.cz/agcac_/modulefiles/26_1/cs-Zadani_1_Vytvoreni-databaze-projektu-materialu-a-jejich-slozeni.pdf

Popis: Vytvoření databáze projektů, materiálů a jejich složení

#### Stávajicí řešení:
- Excelová tabulka o 1348 položkách / 561 technických listů
- Aktualizace tabulky (technických listů) je prováděna ručním zápisem do FILTR_materiálů a FILTR_TL

#### Požadavky:
- Přehled na kterých materiálech se daný materiál / přípravek používá
- Přehled nad tím, z jakých materiálů je daný projekt složen
- Změny v reálném čase na všech zařízeních (socket)
- Přihlašování (guest = čtení ; admin = možnost editace a importování)
- Filtrace materiálu podle technického listu (one-TL has many)
- Filtrace projektů podle čísla materiálu, dílu či přípravku
- Ukládání informací o složení chemických přípravků a materiálů
    - Řádky budou kluzné láky (dle názvu)
    - Sloupce jsou podle složení (např. benzen) + IMDS/BS ID, viz fotka v originálním materiálu
    - Obsahem je procento
- Vyhledávání
    - materiálů podle čísla technického listu
    - materiálů podle názvu projektu
    - projektů podle čísla materiálu (SAP)

- Originální funkčnost
    - reaktivní obsah (pomocí socketů), změny v reálném čase
    - možnost importu stávajícího řešení excel tabulky (EXCEL parse)

#### Cíl
- Vytvoření přehlednější, modernějšího a rychlejšího řešení
- Náhrada stávající Excel tabulky
- Nahradit zastaralý design tabulky a udělat ho hezčím
- Zrychlení procesu hledání a indexace

#### Výstupní materiál
- Funkční program obsahujicí zkušební databázi s daty
    - např. pro 5 projektů 30 různých materiálů
    - lepší alternativou by byla možnost importace staré tabulky z xslx
- API dokumentace
- Návod a dokumentace pro správu a editaci
    - ve formátu PDF/PPTX
    - úprava stávajicích dat, zakládání nových projektů a materiálů
- Prezentace a obhajoba programu
- Jednoduché logo


#### Jednotlivé jména věcí **Filtr Materiálu**
- Kontrola počtu
- Počet materiálu
- najaký OK
- Název projektu Projekt1 etc.
- TL/TDS 1,2,,3,4,etc.
- Sklo SR,QLF,WS,BL,FDF,RDF,RD,FD,FFX,BL,etc. = Typ materiálu (asi) 
- Materiál1,etc. a potom ještě nějaké ID nějaké ID mají jednu nebo více / ID = SAP číslo
- Každý materiál má ano/ne
- Nějaké materiály mají jinou barvu je to kvůli tomu že něco je čistič nebo aktivátor, kluzný lak, Granulát
- Počet materiálu: 116 etc.
  #### Jednotlivé jména věcí **Čističe a aktivátory**
- Čistič 1-10 mby more
- Jestli jsou aktivní nebo ne 

