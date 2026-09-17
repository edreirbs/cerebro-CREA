---
titulo: Vacantes — el pipeline CV a vacantes
tipo: proyecto
proyecto: vacantes
tags: [scrapper, matching]
estado: pausado
actualizado: 2026-09-17
fuentes:
  - "Notion · página «Scrapper», la más reciente de la base · leída 2026-09-17"
  - "Repositorio TheIns07/entrevist-ia · commit e9724fe · búsqueda dirigida 2026-09-17"
relaciones:
  extiende: []
  contradice: []
  depende_de: []
---

# Vacantes

## 1. Estado hoy

**Es el documento mejor escrito del expediente y no tiene una línea de código.**
La página *Scrapper* es la más detallada y la más recientemente editada de todo
el tablero; en el repositorio no hay ni rastro de ella.

## 2. La meta comprometida

**No hay** meta de negocio. La página sí fija objetivos técnicos: cachear
resultados **20–30 minutos**, y *"preparar la beta para miles de usuarios"* —una
intención, sin número ni fecha.

## 3. Numeralias

| Cifra | Valor | Fecha | Fuente |
|---|---|---|---|
| Resultados tras score local | TOP 12 | 2026-09-17 | Notion, diagrama de *Scrapper* |
| Resultados tras rerank con IA | TOP 5 | 2026-09-17 | Notion, *Scrapper* |
| Caché de búsquedas | 20–30 min | 2026-09-17 | Notion, *Scrapper* punto 2 |
| Ejemplo de salida de depuración | 30 resultados de proveedor, 27 únicos | 2026-09-17 | Notion, *Scrapper* punto 7 |
| Líneas de código en el repositorio | **0** | 2026-09-17 | Repo, búsqueda de proveedores y *matching* |

## 4. Hitos

- **2026-09-17** — última edición de *Scrapper*. **El elemento más reciente de
  todo el tablero.**
- **Próximos: ninguno.** No hay fecha de implementación.

## 5. Decisiones tomadas

- **Score local primero, rerank con IA después** — TOP 12 → TOP 5. Reduce costo
  de IA filtrando antes. **Descartada:** no consta.
- **Cachear las búsquedas 20–30 min**, explícitamente *"para preparar la beta"*.
- **Varios proveedores de bolsas de trabajo**, nombrados en la página.

Las tres están **documentadas y ninguna implementada**.

## 6. Compromisos ajenos

Ninguno. Este frente no está bloqueado por nadie: está sin empezar.

## 7. Riesgos y contradicciones abiertas

**R1 · Es el plan más maduro y el producto más ausente.** Que sea lo último
editado sugiere que es donde está la atención hoy; que no tenga código dice que
la atención no se ha convertido en trabajo.

**R2 · El diseño ya fija decisiones de costo** —caché, TOP 12 antes del
rerank— **sin un solo dato real de consumo**. Están tomadas contra una
estimación, no contra una medición.

## 8. Cobertura de esta compilada

Una sola página de Notion y una búsqueda dirigida en el repositorio (proveedores
de empleo, *scrapping*, *matching*). **No se leyó el repositorio entero línea por
línea**, ni hay historial: el clon es superficial. La afirmación *"0 líneas"* es
**resultado de buscar así**, en el commit `e9724fe`; no es una afirmación sobre
todo lo que exista en cualquier rama.

## 9. Fuentes

- 2026-09-17 · Notion, página *Scrapper* · https://inscreup.notion.site/38ce78250e0880d39c33ec11ac0277c9
- 2026-09-17 · Repositorio, commit `e9724fe` · https://github.com/TheIns07/entrevist-ia
