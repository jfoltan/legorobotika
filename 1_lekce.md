## Lekce 1

### 📋 Cheatsheet

| Co chci udělat | Kód |
|---|---|
| Importovat hub | `from pybricks.hubs import PrimeHub` |
| Importovat barvy | `from pybricks.parameters import Color` |
| Importovat čekání | `from pybricks.tools import wait` |
| Vytvořit hub | `hub = PrimeHub()` |
| Rozsvítit LED | `hub.light.on(Color.RED)` |
| Zhasnout LED | `hub.light.off()` |
| Pípnout | `hub.speaker.beep()` |
| Pípnout tón | `hub.speaker.beep(440, 300)` — 440 Hz, 300 ms |
| Počkat | `wait(1000)` — 1000 ms = 1 s |
| Zobrazit číslo | `hub.display.number(42)` |
| Zobrazit ikonu | `hub.display.icon(matice_5x5)` |
| Vypsat do konzole | `print("text")` |
| Opakovat 5× | `for i in range(5):` |
| Opakovat navždy | `while True:` |
| Vytvořit seznam | `barvy = [Color.RED, Color.BLUE]` |
| Projít seznam | `for barva in barvy:` |
| Přečíst tlačítka | `hub.buttons.pressed()` |

**Barvy:** `Color.RED`, `Color.GREEN`, `Color.BLUE`, `Color.YELLOW`, `Color.MAGENTA`, `Color.ORANGE`, `Color.WHITE`, `Color.NONE`

**Frekvence not:** C4=262, D4=294, E4=330, F4=349, G4=392, A4=440, B4=494, C5=523

### Kostra programu

```python
# 1. IMPORTY
from pybricks.hubs import PrimeHub
from pybricks.parameters import Color
from pybricks.tools import wait

# 2. INICIALIZACE
hub = PrimeHub()

# 3. HLAVNÍ PROGRAM
hub.light.on(Color.GREEN)
hub.speaker.beep()
print("Ahoj, FLL!")
wait(2000)
hub.light.off()
```

### 🎯 Mise

- **Mise 1a: Disco Robot** — naprogramuj hub tak, aby blikal různými barvami a pípnutími
- **Mise 1b: Morse kód** — naprogramuj hub, aby vyblikával tvoje iniciály v Morseově abecedě
- **Mise 1c: Hudební nástroj** — pomocí `hub.speaker.beep(frequency, duration)` zahraj melodii
- **🏆 Výzva:** Kdo naprogramuje nejdelší světelnou/zvukovou show?

---