---
name: podar
description: La operación inversa de compilar. Mueve los apéndices históricos fuera de las notas vivas para que vuelvan a responder en segundos. Usar cuando una nota crezca demasiado, cuando la verificación avise "nota grande", o cuando se pida podar, adelgazar o limpiar el vault.
---

# Podar

Compilar agrega. Sin esta operación, las notas crecen por acumulación hasta que
dejan de servir para lo que existen.

El caso que produjo esta skill: una nota de proyecto llegó a **14 apéndices de
compilada apilados, 1,479 líneas y 180 KB**, con los ocho bloques vivos en el
primer 20% y el resto archivo histórico que nadie poda. Esa nota ya no responde
*"¿cómo va X?"* en segundos: hay que buscar dentro de ella.

**Un vault se ahoga en su propio éxito, no en su fracaso.**

---

## Cuándo se poda

Cuando `cerebro verificar` avise `nota grande`, o cuando una nota pase el tope
de `cerebro.json`. **No cuando se vuelva molesta** — para entonces ya dejaste de
leerla, que es precisamente el daño.

---

## Qué se poda y qué no

**Se poda:** los apéndices por fecha (`## Compilada …`, `## Actualización …`),
las listas de citas de sesiones viejas, las contradicciones **ya resueltas** con
su resolución, y los hitos cumplidos de ciclos cerrados.

**No se poda nunca:**

- Los **ocho bloques vivos**. Son la nota.
- Las **contradicciones abiertas**, por viejas que sean. Una contradicción vieja
  no es historia: es un pendiente que nadie ha cerrado.
- Las **decisiones con su alternativa descartada**. Son lo que evita volver a
  discutir lo mismo en seis meses.
- Los **compromisos ajenos abiertos**. Su antigüedad es justo el dato que los
  hace accionables.
- Las **fuentes**. Una cita que se poda es una afirmación que se queda sin
  respaldo.

---

## Cómo se poda

1. **Lee la nota entera** antes de mover nada.
2. Crea o abre `historico/<nombre-de-la-nota>-<año>.md`, con frontmatter propio
   (`tipo: nota`, mismo `proyecto`, `tags: [historico]`).
3. **Mueve** los apéndices ahí, en orden cronológico, **sin resumirlos** — un
   histórico resumido pierde exactamente lo que lo hace útil, que es el detalle
   textual con su fecha.
4. En la nota viva, deja **una línea** al pie: `El detalle de las compiladas de
   <año> vive en [[<nombre>-<año>]].`
5. Enlaza en las dos direcciones.
6. Corre `cerebro verificar` y confirma que no quedó ningún enlace roto.

🔴 **Nada se borra.** Podar es mover, nunca eliminar. Si algo parece que sobra,
va al histórico — no a la basura. Borrar es rojo del semáforo.

🟡 **Si al leer la nota encuentras que un apéndice contiene un hecho que los
bloques vivos no tienen, no lo muevas: súbelo al bloque que le toca primero.**
Podar sin leer es cómo se pierde información.

---

## Cómo entregar

Di cuánto adelgazó cada nota —de X a Y líneas—, qué se movió, y **qué decidiste
NO mover y por qué**. Y ofrece el commit; no lo hagas.
