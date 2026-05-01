<div align="center">

<img src="../../docs/assets/logo.svg" width="132" height="132" alt="Logo TokenGovernor" />

# TokenGovernor

**Disciplina eficiente en tokens para agentes de código IA — reglas que tú controlas.**

[![Licencia: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](../../LICENSE.md)

[Lee en inglés](../../README.md) · [Instalación](INSTALL.md) · [Seguridad](SECURITY.md) · [Índice de idiomas](../README.md)

</div>

---

## Contenidos

- [Resumen](#resumen)
- [Para quién es](#para-quién-es)
- [Qué incluye el kit](#qué-incluye-el-kit)
- [Primeros pasos](#primeros-pasos)
- [Mapa de documentación](#mapa-de-documentación)
- [TokenGovernor Plus](#tokengovernor-plus)

---

## Resumen

**TokenGovernor** es un **kit de reglas** para equipos que desarrollan con asistencia de IA. Ajusta cómo los agentes leen contexto, planifican y piden confirmación antes de operaciones riesgosas — para gastar menos tokens en ruido y más en entregar valor.

**TokenGovernor Lite** (esta edición) es la capa **abierta y solo Markdown**: cópiala en tu repo, conéctala a Cursor, Claude Code, OpenClaw, Gemini CLI, OpenCode u otras herramientas, y los agentes comparten la misma disciplina.

| Obtienes | Detalle |
|----------|---------|
| **Límites de comportamiento** | Lecturas especulativas, volcados de logs y desviación de alcance — no es un motor de cupos duro. |
| **Coherencia multi-herramienta** | Una carpeta `tokengovernor/`: línea base universal, reglas Cursor y **packs** por IDE. |
| **Memoria de proyecto opcional** | **`workspace-memory/`** notas por niveles (north star, temas, decisiones). |

**Importante:** los archivos que leen los modelos (`universal/`, `cursor/`, `packs/`) están en **inglés** por convención. Esta carpeta **`i18n/`** es documentación **para personas**.

---

## Para quién es

- Equipos que quieren **comportamiento predecible** del agente entre Cursor, Claude, Gemini, OpenCode, OpenClaw o similares.
- Proyectos donde la **higiene de contexto** importa para coste y revisión.
- Quienes prefieren **reglas como archivos en Git** frente a un panel alojado.

---

## Qué incluye el kit

| Ruta | Función |
|------|---------|
| **`universal/TOKEN_GOVERNOR_LITE.md`** | Línea base: no negociables, aprobaciones, forma de respuesta. |
| **`cursor/rules.md`** | Reglas Cursor alineadas con la base. |
| **`packs/`** | Reglas por herramienta, comandos de sesión, memoria, seguridad, ejemplo. |
| **`workspace-memory/`** | Notas duraderas opcionales ([README](../../workspace-memory/README.md)). |
| **`docs/`** | [Glosario](../../docs/GLOSSARY.md), [Resolución de problemas](../../docs/TROUBLESHOOTING.md) (inglés). |

Resumen humano de **`packs/`** en español: [PACKS-OVERVIEW.md](PACKS-OVERVIEW.md).

---

## Primeros pasos

1. Sigue **[INSTALL.md](INSTALL.md)** (copia, submódulo, estructura, texto para pegar en el agente).
2. Problemas: **[docs/TROUBLESHOOTING.md](../../docs/TROUBLESHOOTING.md)** (inglés).
3. Términos: **[docs/GLOSSARY.md](../../docs/GLOSSARY.md)** (inglés).

---

## Mapa de documentación

| Documento | Uso |
|-----------|-----|
| [INSTALL.md](INSTALL.md) | Instalación |
| [UPGRADE.md](../../UPGRADE.md) | Actualizaciones (inglés) |
| [CONTRIBUTING.md](../../CONTRIBUTING.md) | Contribuir (inglés) |
| [CHANGELOG.md](../../CHANGELOG.md) | Historial (inglés) |
| [SECURITY.md](SECURITY.md) | Divulgación responsable |

---

## TokenGovernor Plus

**Plus** (desde **$9/mes**) incluye la misma base de comportamiento con **CLI `tg`**, packs ampliados y benchmarks. Detalles e instalación: **[TokenGovernor Plus](https://github.com/gokubingoman/tokengovernor-plus)**.

---

## Licencia

MIT — ver [LICENSE.md](../../LICENSE.md).
