# 🤖 Cheatsheet: Python + Pybricks

> Najdeš tu vysvětlení syntaxe, cheatsheety ke každé lekci, zadání misí a přípravu na kvízy.

---

## 📖 Jak číst a psát Python — referenční příručka

> Vracej se sem kdykoli potřebuješ. Toto je tvůj **slovníček a gramatika** jazyka Python.

---

### 1. Hodnoty a datové typy

| Typ | Český název | Příklad | Poznej podle |
|-----|-------------|---------|--------------|
| `int` | Celé číslo | `42`, `-3`, `0` | Žádná tečka, žádné uvozovky |
| `float` | Desetinné číslo | `3.14`, `-0.5` | Má desetinnou **tečku** (ne čárku!) |
| `str` | Text (string) | `"Ahoj"`, `'FLL'` | Vždy v **uvozovkách** `"..."` nebo `'...'` |
| `bool` | Pravda/nepravda | `True`, `False` | S velkým písmenem! |
| `None` | Nic / prázdno | `None` | „tady nic není" |

```python
vek = 14              # int
pi = 3.14             # float
jmeno = "Robot"       # str
je_pripojeny = True   # bool
```

> 💡 **String** = cokoli v uvozovkách. `"..."` i `'...'` je OK. Bez uvozovek si Python myslí, že je to proměnná!

---

### 2. Proměnné — krabičky se štítkem

```python
rychlost = 500           # do krabičky "rychlost" vlož 500
nazev = "Super Robot"    # do krabičky "nazev" vlož text
hub = PrimeHub()         # do krabičky "hub" vlož objekt
```

**Pravidla:** písmena + číslice + `_`, nesmí začínat číslem, bez mezer, bez diakritiky.

---

### 3. Tečková notace — nejdůležitější vzor!

Tečka `.` = „vezmi věc nalevo a přistup k její vlastnosti."

```
hub.light.on(Color.GREEN)
│    │     │
│    │     └── funkce: „rozsvítit"
│    └──────── vlastnost: světlo
└───────────── objekt: hub
```

Jako adresa: **Česko.Brno.Masarykova** — zpřesňuješ kam míříš.

```python
hub.speaker.beep()           # hub → reproduktor → pípni
hub.display.number(42)       # hub → displej → zobraz číslo
Color.RED                    # modul Color → hodnota RED
Port.A                       # modul Port → port A
```

> 🎯 Čti tečku jako „jejího/jeho": `hub.light.on()` = „hubův light, jeho on".

---

### 4. Funkce — příkazy se závorkami

```
hub.speaker.beep(440, 300)
│              │    │    │
│              │    │    └── 2. parametr: trvání
│              │    └─────── 1. parametr: frekvence
│              └──────────── název funkce
└─────────────────────────── objekt
```

```python
hub.light.off()              # 0 parametrů
hub.light.on(Color.GREEN)    # 1 parametr
hub.speaker.beep(440, 300)   # 2 parametry
```

**Funkce co vrací hodnotu:**
```python
stisknuta = hub.buttons.pressed()   # uloží výsledek
uhel = hub.imu.heading()            # uloží číslo
```

---

### 5. Závorky — tři druhy

| Závorka | Kdy se používá | Příklad |
|---------|----------------|---------|
| `()` | Funkce, tuple | `beep()`, `(440, 300)` |
| `[]` | Seznamy, index | `[1, 2, 3]`, `barvy[0]` |
| `{}` | Slovníky | `{"jmeno": "Robot"}` |

---

### 6. Odsazení = syntaxe!

```python
for i in range(3):
    hub.speaker.beep()     # ← 4 mezery = patří do cyklu
    wait(500)              # ← 4 mezery = taky do cyklu
hub.light.off()            # ← bez odsazení = PO cyklu
```

⚠️ Špatné odsazení = **chyba** (IndentationError)!

---

### 7. Komentáře

```python
# Toto Python ignoruje — slouží tobě
hub.light.on(Color.GREEN)    # komentář na konci řádku
```

---

### 8. Importy

```python
from pybricks.hubs import PrimeHub     # z balíčku vytáhni nástroj
from pybricks.parameters import Color
from pybricks.tools import wait
```

---

### 9. Operátory

```python
rychlost = 500       # = přiřazení: „ulož"
rychlost == 500      # == porovnání: „je rovno?" → True/False

# Porovnání: ==, !=, <, >, <=, >=
# Logické: and, or, not
# Matika: +, -, *, /, //, %
```

⚠️ **Nejčastější chyba:** `=` místo `==` v podmínce!

---

### 10. Podmínky

```python
if barva == Color.RED:
    print("Stůj!")          # dvojtečka + odsazení!
elif barva == Color.GREEN:
    print("Jeď!")
else:
    print("Neznámá")
```

---

### 11. f-string

```python
jmeno = "Robot"
print(f"Jmenuji se {jmeno}")    # → Jmenuji se Robot
```

---

### 🗺️ Mapa syntaxe

```
Python program
├── import .............. from X import Y
├── proměnná ........... jmeno = hodnota
├── funkce ............. objekt.funkce(param)
├── komentář ........... # text
├── if/elif/else ....... podmínka:
├── for ................ for x in kolekce:
├── while .............. while podmínka:
├── int ................ 42
├── str ................ "text"
├── list ............... [1, 2, 3]
└── tuple .............. (440, 300)
```

---

### ⚠️ Top 5 chyb

| # | Chyba | Řešení |
|---|-------|--------|
| 1 | Chybějící `:` | `for i in range(5):` ← dvojtečka! |
| 2 | Špatné odsazení | Vždy 4 mezery |
| 3 | `=` místo `==` | `if x == 5:` ← dvě rovnítka! |
| 4 | Chybějící uvozovky | `print("Ahoj")` ← uvozovky! |
| 5 | Chybějící závorky | `hub.speaker.beep()` ← závorky! |

---