## Lekce 3 — Motory: Robot se hýbe!

### 📋 Cheatsheet

| Co chci udělat | Kód |
|---|---|
| Levý motor | `Motor(Port.A, Direction.COUNTERCLOCKWISE)` |
| Pravý motor | `Motor(Port.B)` |
| Běž (neblokující) | `motor.run(500)` |
| Běž po dobu | `motor.run_time(500, 2000)` |
| Otoč o úhel | `motor.run_angle(500, 360)` |
| Zastav | `motor.stop()` / `brake()` / `hold()` |
| Vynuluj enkodér | `motor.reset_angle(0)` |
| Přečti enkodér | `motor.angle()` |

**Vzdálenost (mm) = (úhel / 360) × π × průměr_kola**

**Směry:** L vpřed + R vzad = otáčení vpravo; L vzad + R vpřed = vlevo

**Blokující vs. neblokující:**
- `run_angle(500, 360)` → čeká, až se motor otočí
- `run(500)` → motor běží, program pokračuje → musíš `stop()`

### 🎯 Mise

- **Mise 3a: Rovná jízda** — přesně 50 cm
- **Mise 3b: Čtverec** — výpočet úhlů
- **Mise 3c: Písmena** — iniciály jízdou
- **Mise 3d: Parkour** — kombinace
