# liška-husa-pytel-se-zrním

Jde o jednu z oblíbených hádánek Lewise Carolla. Hříčka se točí kolem lišky, husy a pytle zrní. Vše spočívá v tom, dostat je bezpečně na druhý konec řeky.

# Pravidla

Pravidla této úlohy jsou:

- Musíte dostat lišku, husu a zrní bezpečně na druhý břeh řeky
- V jednu chvíli můžete mít s sebou na člunu pouze jednu položku
- Liška nesmí zůstat sama na břehu s husou, (protože tento stav by pro husu neměl dlouhého trvání)
- Husa nesmí zůstat na břehu sama se zrním, (protože by to pro změnu nedopadlo úplně dobře pro zrní)

Datová struktura reprezentující řešení je vektor vektorů.

Začínáme ve stavu, kdy jsou všechny předměty na levé straně řeky. Člun je prázdný, druhý břeh řeky taktéž.

```clojure
[[[:liska :husa :zrni :ja] [:clun] []]]
```
Můžeš s sebou vzít kupříkladu zrní

```clojure
[[[:liska :husa :zrni :ja] [:clun] []]
[[:liska :husa] [:clun :zrni :ja] []]]
```

Ale v tom případě liška sežere husu!

Cílem je naplánovat kroky tak, ať se všichni bezpečně dostanou na opačnou stranu

```
[[[:liska :husa :zrni :ja] [:clun] []] // počáteční stav
...
[[[] [:clun] [:liska :husa :zrni :ja]]]] // cílový stav
```

Počet ani jména položek se během testování nebudou dynamicky měnit. Vždy se bude pracovat pouze s `:ja`, `:liska`, `:husa`, `:zrni`, `:clun`.

# Instrukce

- Příkaz `make run` vytiskne výstup na `stdout` (standardní výstup). Výstup by měl vypadat zhruba takto:
```
Mac-Book-Pro:mymac ~ $ make
[[[:liska :husa :zrni :ja] [:clun] []]
...
[[[] [:clun] [:liska :husa :zrni :ja]]]]
```

- Nejsou zde žádné limitace na programovací jazyk. Pokud používáš něco exotického, přidej Makefile příkaz `make install` na instalaci všech potřebných závislostí, které nejsou v základu na Mac OS dostupné.
- Jde o programovací úlohu a řešení s prostými `print()` výrazy nebude považováno jako validní a akceptovatelné řešení.
