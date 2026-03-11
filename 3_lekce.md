## Lekce 4 — DriveBase: Řízení jako profík

### 📋 Cheatsheet

| Co chci udělat     | Kód                                                                 |
| ------------------ | ------------------------------------------------------------------- |
| Vytvořit DriveBase | `robot = DriveBase(left, right, wheel_diameter=56, axle_track=112)` |
| Rovně              | `robot.straight(200)` — 200 mm                                      |
| Vzad               | `robot.straight(-200)`                                              |
| Otočit             | `robot.turn(90)` — 90° doprava                                      |
| Oblouk             | `robot.curve(200, 90)` — r=200mm, 90°                               |
| Plynulá jízda      | `robot.drive(200, 0)` — 200 mm/s, nečeká                            |
| Zastavit           | `robot.stop()`                                                      |
| Rychlost           | `robot.settings(straight_speed=200, turn_rate=100)`                 |
| Reset počítadel    | `robot.reset()`                                                     |
| Ujetá vzdálenost   | `robot.distance()` mm                                               |
| Úhel otočení       | `robot.angle()` °                                                   |

**Kalibrace:** `wheel_diameter` = přesnost vzdálenosti, `axle_track` = přesnost otáčení.

**Kalibrace postup:**

1. `robot.straight(1000)` — ujel víc? zmenši diameter. Méně? Zvětši.
2. `robot.turn(3600)` — víc než 10 otoček? zvětši axle_track.
3. Ověř čtvercem: 4× `straight(500)` + `turn(90)`.

### 🎯 Mise

- **Mise 4a: Slalom** mezi překážkami
- **Mise 4b: Kalibrace** — měření a ladění
- **Mise 4c: Oblouky** — esíčko pomocí `curve()`
- **🏆 Výzva: Závod přesnosti** (body za přesnost, ne rychlost)