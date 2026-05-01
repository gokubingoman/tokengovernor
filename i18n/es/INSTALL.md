# Instalación — TokenGovernor Lite

TokenGovernor Lite se distribuye como **Markdown y recursos** — sin instalador. Copia la carpeta en el repositorio de tu aplicación y enlaza cada herramienta de IA a las rutas indicadas.

[Volver al README en español](README.md) · [English](../../INSTALL.md)

---

## Opción A — Copiar

```bash
git clone https://github.com/gokubingoman/tokengovernor.git
cp -r tokengovernor/{universal,cursor,packs,workspace-memory} /ruta/a/tu-proyecto/third_party/tokengovernor
```

**Cursor:** reglas del proyecto → `third_party/tokengovernor/cursor/rules.md`.  
**Claude, Gemini, OpenCode, OpenClaw:** abre los archivos bajo `packs/` según la documentación de cada herramienta (los textos de reglas están en **inglés**).

---

## Opción B — Submódulo Git

```bash
cd /ruta/a/tu-proyecto
git submodule add https://github.com/gokubingoman/tokengovernor.git third_party/tokengovernor
```

Fija el submódulo a un tag o commit para actualizaciones reproducibles.

---

## Estructura recomendada

Un directorio (a menudo **`tokengovernor/`**) con:

| Carpeta | Contenido |
|---------|-----------|
| **`universal/`** | `TOKEN_GOVERNOR_LITE.md` |
| **`cursor/`** | `rules.md` |
| **`packs/`** | Packs por herramienta, comandos, memoria, seguridad |
| **`workspace-memory/`** | Notas por niveles (recomendado) |

Las rutas dentro del Markdown asumen este diseño. Si renombras la carpeta, actualiza referencias cruzadas.

---

## Primera sesión (pegar en el agente)

```txt
Apply TokenGovernor from tokengovernor/universal/TOKEN_GOVERNOR_LITE.md and tokengovernor/cursor/rules.md.
Use low-token discipline: no default full-repo scans; plan before multi-file edits.
```

(Mantén el texto en **inglés** para mayor consistencia con los archivos de reglas.)

---

## Memoria de proyecto

Usa **`workspace-memory/`** para contexto no secreto: `north-star.md`, `_index.md`, `topics/`, `decisions/`. Política: **`packs/memory/tiered-context-loading.md`**, **`packs/memory/retrieval-first-memory.md`**.

---

## TokenGovernor Plus

Con **Plus**, instala con el CLI **`tg`** (`tg init`, `tg memory-init`, `tg doctor`) desde tu distribución Plus. Plus **no** es obligatorio para usar Lite.

---

## Problemas

Ver **[docs/TROUBLESHOOTING.md](../../docs/TROUBLESHOOTING.md)** (inglés).
