---
titulo: Conexiones entre frentes
tipo: nota
proyecto: transversal
tags: [conexiones, transversal]
actualizado: 2026-09-17
fuentes:
  - "Barrido del 2026-09-17 sobre los cuatro frentes compilados"
relaciones:
  extiende: []
  contradice: []
  depende_de: []
---

# Conexiones entre frentes

> Aquí viven las conexiones, **no dentro de la nota de un frente**: si viven en
> uno solo, el otro nunca se entera.
>
> **La vara, y se cumplen las tres o no entra:** no es obvia leyendo un solo
> frente · cita textualmente los dos lados con fecha y fuente · tiene una
> consecuencia accionable.

**Primer barrido con más de un frente compilado: 2026-09-17.** Los cuatro
anteriores declararon "ninguna" porque solo había un frente. Ahora hay tres.

---

## C-01 · El tablero le va a reportar al programa cero avance sobre un proyecto que sí avanzó

**Lado A — [[incubacion]].** La columna de estado del tablero dice *Not started*
en **17 de 17 filas**, y `Priority` solo cubre 14 de 17. Leído 2026-09-17.

**Lado B — [[entrevista]].** El repositorio tiene commit del **2026-09-16**, la
entrevista por voz está implementada —componente, servicio de transcripción y
edge function— y tres páginas del tablero tienen trabajo escrito. Leído
2026-09-17.

**Por qué no es obvia desde un solo frente.** Quien mira el tablero ve un
proyecto detenido y no tiene motivo para dudar. Quien mira el repositorio ve
avance y no sabe qué se está reportando en su nombre.

**Consecuencia accionable.** El sprint cierra en diciembre y el tablero es lo
que un programa de incubación mira para evaluar. **Actualizar los estados cuesta
minutos; que te evalúen por un tablero que dice cero, cuesta el caso.**

---

## C-02 · El riesgo comercial no se arregla reescribiendo la copy: se arregla desplegando

**Lado A — [[comercial]].** La landing promete *"Respondes en voz alta a un
entrevistador con IA"* y muestra un testimonial de *"contratada en 2 semanas"*.
Leído del bundle, 2026-09-17.

**Lado B — [[entrevista]].** La voz **ya está construida** en el repositorio —
`getUserMedia`, `MediaRecorder`, `AudioContext`, más la edge function
`transcribe-audio`— y **no está en el bundle desplegado**. Leído 2026-09-17.

**Por qué no es obvia desde un solo frente.** Leyendo solo Comercial, la
conclusión natural es *"baja la promesa, el producto no la cumple"*. Leyendo
solo Entrevista, es *"hay que desplegar cuando se pueda"*. Juntas dicen otra
cosa: **la promesa ya es verdad, solo que no está publicada.**

**Consecuencia accionable.** Un despliegue cierra el riesgo comercial **sin
tocar una palabra del mensaje**. Bajar la promesa habría sido destruir valor que
ya está construido.

**Lo que NO cierra.** El informe de resultados sigue siendo fijo — todos ven
6.4. Eso sí es promesa sin producto, y sigue abierto en [[entrevista]], R1.

---

## Descartada en este barrido

**«Ningún frente tiene meta.»** Es cierto en los cuatro, pero **no es una
conexión: es una ausencia compartida.** No cita dos lados que se iluminen entre
sí; ya está declarada en `CLAUDE.md` §4 y repetirla aquí sería inflar el conteo.

**«Vacantes es el plan más reciente y no tiene código.»** No pasa la primera
condición: se ve entero leyendo [[vacantes]] sola. Es un riesgo de ese frente,
no una conexión.
