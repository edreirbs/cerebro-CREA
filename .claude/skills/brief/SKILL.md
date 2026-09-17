---
name: brief
description: Lee juntos los compromisos ajenos de todos los frentes y arma la vista de quién debe qué, desde cuándo y a quién bloquea. Usar antes de una junta de seguimiento, cuando se pida el brief, el estado de todo, los pendientes ajenos o qué está trabado.
---

# Brief

Las notas de proyecto tabulan los compromisos ajenos frente por frente. Esta
skill los **lee juntos**, que es lo que nunca pasa solo.

El problema que resuelve: con cuatro frentes, los bloqueadores viven repartidos
en cuatro archivos y **nadie los mira nunca en la misma pantalla**. Un
compromiso que lleva cinco meses abierto se ve igual de urgente que uno de la
semana pasada mientras estén en notas distintas.

**Esta skill no compila nada.** Solo lee y ordena. No modifica ninguna nota.

---

## Qué hace

1. Recorre el bloque **Compromisos ajenos** de cada nota en `proyectos/`, y los
   de las notas que declaren tenerlos.
2. Normaliza cada uno a: **quién debe · qué · desde cuándo · a quién bloquea ·
   en qué frente · fuente**.
3. **Ordena por antigüedad**, no por frente. Ése es el punto: lo que lleva más
   tiempo abierto sube.
4. Agrupa por persona al final, para responder *"¿qué le pido a esta persona
   cuando la vea?"* — que es la pregunta con la que se usa el brief en la vida
   real.

---

## Las tres señales que hay que subrayar

**a) Una persona que aparece en dos o más frentes.** Deja de ser un pendiente y
es un cuello de botella. Nómbralo así.

**b) Dos personas distintas que reportan a la misma.** Si dos frentes se traban
con dos personas que tienen un jefe común, **esa tercera persona es una sola
conversación en vez de dos escalamientos**. Es la palanca más eficiente que hay
y casi nunca se ve mirando un frente a la vez.

**c) Un compromiso vencido cuya fecha ya pasó sin que nadie lo dijera.** Un
compromiso intra-semana que no se verifica **se da por cumplido por omisión**,
que es la manera más silenciosa de perder un acuerdo. Si hay registro de la
sesión donde debía retomarse, búscalo ahí y declara si se ejecutó o no.

Cuando no aparezca, decláralo como **inferencia por ausencia**, marcada como
tal. No es lo mismo *"se decidió lo contrario"* que *"no se mencionó"*: lo
segundo se arregla con un mensaje y lo primero no.

---

## Cómo entregar

Conclusión adelante: **cuántos compromisos abiertos, cuál es el más viejo, y
quién concentra más**.

Después la lista por antigüedad, y al final el agrupado por persona.

**Sin tablas si quien lo lee las va a copiar y pegar** — revísalo en
`CLAUDE.md`.

Y una línea final: **las tres conversaciones que más destraban**, nombradas.
