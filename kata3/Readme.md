# daruj život

Život je těžký a složitý. Někdy ale dokáže být dokáže velmi jednoduchý. Tak jednoduchý, že jej dokážeme udržet při životě pomocí několika pravidel ...

# Zadání

Vaším úkolem je napsat program, který vypočítá následující generace hry života nalezené prof. Conwayem (Conway's Game of Life). Začínáme s dvoudimenzionální mřížkou buňek. Každá buňka může být buďto živá nebo mrtvá. Mřížka je konečná a mimo její hranice neexistuje žádný život. Další generaci mřížky vypočítáme podle následujících pravidel:

1. Pokud má živá buňka méně než dva sousedy, umírá v osamění.
2. Pokud má živá buňka více než 3 sousedy, umírá přeplněním.
3. Pokud má živá buňka 2 nebo 3 sousedy, přežívá do další generace.
4. Pokud má mrtvá buňka přesně 3 sousedy, v další generaci ožívá.

Jako sousední buňky považujeme ty, které se nacházejí v osmiokolí dané buňky.

# Příklad

- `*` - indikuje živou buňku
- `.` - indikuje mrtvou buňku

Generace 1 (mřížka 4x8):
........
....*...
...**...
........

Generace 2:
........
...**...
...**...
........

# Instrukce

Přidejte `Makefile` s následujícími příkazy:
- `install` - nainstaluje všechny závislosti potřebné k běhu programu (můžete přeskočit pokud jsou v základních utilitách macOS)
- `build` - zkompiluje zdrojový kód do spustitelného souboru (pokud není potřeba nic kompilovat, tento krok přeskočte)
- `run` - spustí program a na `stdout` (standadní výstup) vytiskne 10 generací života, jehož definice je v souboru specifikovaném v argumentu:

```
Mac-Book-Pro:mymac ~ $ make FILEPATH=zygotes/1.txt run
Zygote
.....
..*..
..*..
..*..
.....
Generation: 1
.....
.....
.***.
.....
.....
Generation: 2
// ...

```

V adresáři `/zygotes` se nachází příklady počátků různých životů.
