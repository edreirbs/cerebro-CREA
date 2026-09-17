# Bitácora

Qué se compiló, **qué no se compiló y por qué**, y qué quedó marcado para
revisar. Se agrega arriba: lo más reciente primero.

> Esto es un cuaderno de laboratorio, no un changelog. Los errores propios se
> registran con la misma prominencia que los aciertos — son los que producen las
> reglas de `meta/decisiones.md`.

> Cuando pase de unas 600 líneas, se corta por año a `meta/bitacora/<año>.md`.
> La compilada solo lee las últimas tres entradas; el resto es histórico.

---

## 2026-09-17 (7) — Paso 5: los tres frentes restantes, y el primer barrido de conexiones real

**Qué se compiló.** `comercial`, `incubacion` y `vacantes`, con la regla nueva
puesta: **ninguna ausencia se escribió sin una segunda verificación citada**.
`cerebro verificar` cierra en **0 errores y 0 advertencias** — los dos enlaces
rotos desaparecieron solos al existir las notas que faltaban.

**Dos conexiones pasaron la vara, y es la primera vez.** Los cuatro barridos
anteriores declararon «ninguna» honestamente: con un frente no hay nada que
cruzar. Van en `notas/conexiones.md`.

- **C-01.** El tablero dice *Not started* en 17 de 17 mientras el repositorio
  commiteó el 2026-09-16 y la voz ya está construida. **Al programa se le va a
  reportar cero avance sobre un proyecto que sí avanzó**, y el sprint cierra en
  diciembre.
- **C-02.** La landing promete voz; la voz **ya existe y solo no está
  desplegada**. Leyendo Comercial sola la conclusión sería *"baja la promesa"*;
  juntas dicen lo contrario: **un despliegue cierra el riesgo sin tocar el
  mensaje**. Bajar la promesa habría destruido valor ya construido.

**Dos candidatas descartadas, y se dice cuáles.** *"Ningún frente tiene meta"* es
una ausencia compartida, no una conexión. *"Vacantes es el plan más reciente sin
código"* se ve entera leyendo un solo frente.

**Qué NO se compiló.** `comercial` es la nota más pobre del vault y se declara
así: **3 filas de Notion, 0 con cuerpo**. Lo único con texto es copy de
marketing. Miro y Figma —donde suele vivir el pitch— siguen cerrados. De
`incubacion`, no se buscó nada del programa CREA fuera de esa base: **no es que
no exista, es que no se entregó fuente y no se buscó.**

**Sobre la proporción que se midió en el alto.** Era 3.7 : 1 a favor de la capa
meta. Esta vuelta agregó cuatro notas de conocimiento y una entrada de bitácora:
va en la dirección correcta. Se vuelve a medir en la próxima compilada.

**Qué queda marcado para quien decide.**

1. **Actualizar los estados del tablero.** Cuesta minutos y es lo que el
   programa mira para evaluar. Es el hallazgo más barato de todo el día.
2. **Desplegar lo que ya está en el repositorio.** Cierra C-02 sin tocar el
   mensaje comercial.
3. **El 6.4 fijo sigue en producción**, y eso sí es promesa sin producto.


## 2026-09-17 (6) — ALTO: auditoría del piloto (paso 3 del arranque)

**El paso que no se puede saltar, hecho.** Las tres preguntas, con números:

| Pregunta | Respuesta |
|---|---|
| ¿Cuántos archivos produjo? | 6 · **una sola nota de conocimiento** (202 líneas) |
| ¿Cuánto pesa la capa meta? | **759 líneas** — decisiones 473, bitácora 286 |
| Proporción meta : conocimiento | **3.7 a 1**, a favor del vault hablando de sí mismo |
| ¿Cuántos se van a releer? | La nota y el contrato. De la bitácora, 3 entradas. De decisiones, **13 en un día: nadie** |
| ¿Qué reglas resultaron falsas? | **Tres**, todas propias |

**Las tres reglas falsas son una sola.** El despliegue no refleja el producto ·
el universo no es el que te entregan · un bloqueo no es falta de permiso.
Las tres tienen la misma forma: **afirmar sin verificar en qué capa estoy
mirando**. Y las tres se corrigieron tarde — por evidencia nueva o porque me
cuestionaron.

**El síntoma medible:** **3 de las 5 entradas anteriores de esta bitácora son
correcciones de errores propios**, no compiladas. El ciclo corrió al revés:
compilar → publicar → que me corrijan.

**La corrección, y es una regla en vez de tres:** antes de escribir cualquier
ausencia —*no existe, no está construido, no hay acceso*— **una verificación más,
en otra capa, citada en la nota**. Sin esa segunda capa no se escribe la
ausencia: se escribe el hueco.

**Lo que esto cambia para el paso 5.** Escalar a `comercial` e `incubacion` con
el ciclo al revés habría multiplicado por cuatro el mismo error — que es
literalmente la razón por la que este alto existe. Se escala **con la regla
nueva puesta**, no antes.

**Lo que NO se corrige:** nada de lo ya escrito. La bitácora es histórica y
`decisiones.md` se agrega, no se reescribe. Lo que cambia es el método de aquí
en adelante.

**Advertencia para la siguiente compilada:** si la proporción 3.7 : 1 no se ha
invertido, el problema no es el registro — es que el vault no está compilando
conocimiento, solo administrándose a sí mismo.


## 2026-09-17 (5) — Cuestionado el diagnóstico de acceso, resultó mal

**Qué pasó.** Se reportó que los tres bloqueos eran falta de permiso. Quien
opera el vault respondió que los enlaces **sí venían con permiso de lectura**.
Al medirlo, tenía razón.

**Lo que se midió, y es lo que había que haber medido antes.**

- **Figma.** `whoami` devuelve la cuenta **institucional `@tec.mx`**, que
  pertenece a **un solo plan** —su propio equipo, tier starter— y no al del
  archivo. Y el error de lectura nunca dijo *"no tienes acceso"*: dice
  ***"no tienes acceso de edición; el dueño puede hacerte editor"***. **El
  conector de Figma exige asiento de editor. Ser lector no alcanza.**
- **Miro.** La cuenta del conector busca «entrevist» entre sus tableros:
  **0 de 0**. El tablero no está en su equipo.

**La regla que salió.** Es el **tercer** error de capa del día, y el más caro de
los tres en consecuencias humanas: los dos anteriores produjeron una nota falsa,
éste habría producido **un reclamo injusto a una contraparte que sí hizo su
parte**. Un bloqueo de acceso se reporta con **tres datos o no se reporta**: con
qué cuenta se intentó, qué nivel de permiso pedía la herramienta, y el error
textual.

**Y una bandera que apareció de paso.** El conector de Figma corre con la cuenta
`@tec.mx`. Material de CREA —que no es del Tec— se leería con infraestructura
institucional: es el cruce que el método prohíbe, y el mismo que este vault ya
resolvió para git y para el repositorio. Queda anotado en `meta/decisiones.md`.

**Qué NO se compiló.** Nada nuevo; esta vuelta fue corrección. Miro y Figma
siguen sin leerse, pero ahora con el remedio correcto anotado: **editor** en
Figma, y **entrar al equipo** en Miro, los dos para la cuenta del conector.

**Conexiones entre frentes: ninguna que pase la vara, y se dice.**


## 2026-09-17 (4) — El vault rechaza por primera vez

**Qué se decidió.** El producto de vacantes hallado en Netlify **no entra**: no
es de CREA. Se sacó de la lista blanca, de `cerebro.json` y de
`proyectos/entrevista.md`, y se nombra sin enlace ni detalle.

**Por qué es la entrada más importante hasta ahora.** Es la primera vez que este
vault ejerce lo único que lo separa de un archivero: **decir que no**. Y el error
que lo produjo es mío y de forma conocida — decidir si algo nuevo pertenece a un
frente es **rojo del semáforo**, y lo traté como amarillo: lo compilé y luego
avisé, en vez de preguntar y luego compilar.

**Consecuencia sobre el frente `vacantes`:** vuelve a ser **plan, no producto**.
Existe como documento de Notion y nada más.

**Lo que NO se borró, y es a propósito.** La entrada (3) de esta bitácora se
queda como está. La bitácora es cuaderno de laboratorio: los errores propios se
registran con la misma prominencia que los aciertos, y corregirla borraría la
única evidencia de cómo se llegó aquí. Lo que se corrige son las **capas vivas**
—contrato, configuración y nota—, que ya se corrigieron todas.

**Lo que sigue pendiente de una persona:** si además hay que **borrar el sitio en
Netlify**. Eso no lo toqué: destruir un despliegue en vivo no se deshace, y no es
lo mismo que sacarlo del vault.

**Conexiones entre frentes: ninguna que pase la vara, y se dice.**


## 2026-09-17 (3) — Barrer la cuenta de Netlify refuta a las dos compiladas anteriores

**Qué se compiló.** Nada nuevo: se **corrigió**. Entró Netlify como sexto
contenedor y se enumeraron sus **8 proyectos**, que es lo que no se había hecho.

**Dos hallazgos, y el segundo vuelve a ser un error propio.**

1. **El sitio de EntrevistIA no está en la cuenta conectada.** Los 8 proyectos
   del equipo no lo incluyen: se despliega desde otra cuenta. Es la **tercera**
   fuente cerrada, junto con Miro y Figma.
2. **«Radar Laboral» (`jobinderai.netlify.app`) sí está, y es el frente
   Vacantes desplegado.** Sube CV en PDF/TXT/MD, extrae el perfil, lo deja
   revisar, y devuelve *"una vacante hot, una internacional, una cercana a tu
   mercado y una reserva ampliada desde varias bolsas activas"*, con entrada por
   Google e historial guardado. La compilada de la mañana había escrito que el
   pipeline de vacantes era *"plan puro, cero rastro"*. **Falso.**

**La regla que salió, y corrige a la de hace unas horas.** Ésta es la segunda
afirmación de ausencia falsa del día, y las dos tienen la misma forma: *el
universo examinado era el de los enlaces recibidos*. La regla de la mañana
ordenaba las capas —repositorio sobre despliegue sobre Notion— pero daba por
buena la lista de objetos dentro de cada capa. La nueva: **se enumera el
contenedor completo antes de escribir cualquier ausencia, y se declara cuántos
objetos se enumeraron, no solo cuántos se leyeron.**

**Qué NO se compiló.** `vacantes` **no se abrió como nota**, aunque ya haya
material real: el paso 2 del arranque manda un solo frente hasta auditar el
piloto, y el piloto lleva dos correcciones en un día — es exactamente el momento
en que escalar multiplica errores. El enlace `[[vacantes]]` queda roto a
propósito.

**Hueco declarado.** Qué bolsas de trabajo usa Radar Laboral **no se pudo
verificar**: su cliente solo llama a `/api/recommendations` y
`/api/search-history`, y el pipeline corre del lado servidor. **No es una
ausencia, es un hueco** — se cierra con acceso a su repositorio.

**Conexiones entre frentes: ninguna que pase la vara, y se dice.** Sigue habiendo
un solo frente compilado.

**Qué queda marcado para quien decide.**

1. **¿Radar Laboral es parte de EntrevistIA o un producto hermano?** De eso
   depende si la lista blanca de cuatro frentes sigue siendo la correcta.
2. **Tres de seis fuentes están cerradas.** Miro, Figma y ahora el Netlify de
   EntrevistIA.
3. Siguen en pie el 6.4 en producción y el 404 por falta de reglas de SPA.


## 2026-09-17 (2) — El repositorio entra como fuente, y refuta a la compilada anterior

**Qué se compiló.** Se agregó el repositorio del producto como **quinta fuente y
primera en autoridad**, y se recompiló entero `proyectos/entrevista.md` contra
él. Clon superficial del commit `e9724fe` (2026-09-16).

**El hallazgo principal es que esta bitácora se refuta a sí misma una entrada
antes.** La compilada de hoy en la mañana afirmó que la entrevista por voz *"no
estaba construida"*, con cero ocurrencias de las APIs de audio en el bundle. En
el repositorio están: un componente de voz, un servicio de transcripción y una
edge function `transcribe-audio`. **La afirmación era falsa, y el error no
estuvo en el dato sino en la capa que se leyó** — un bundle desplegado es una
foto vieja del código. De ahí salió la regla del día en `meta/decisiones.md`:
orden de autoridad **repositorio → despliegue → Notion**, y ninguna ausencia se
escribe sin haberla buscado en el repositorio.

**Las otras tres contradicciones: confirmadas, y dos empeoran.**

- **C2, la evaluación.** No era un residuo del bundle viejo: `ResultsPage.tsx`
  importa de `src/mocks/mockResults.ts`, con `score: 6.4` escrito a mano, y el
  dashboard hace lo mismo dos veces más. **La rúbrica de 7 dimensiones que
  Notion documenta no existe en el código.**
- **C3, la infraestructura.** Aquí el error es de Notion: el código no menciona
  Cloudflare ni una vez y usa **4 tablas**, no 6.
- **C4, las vacantes.** Plan puro. Cero rastro de proveedores de empleo o
  *matching* en todo el repositorio.

**Y una causa localizada.** El 404 de las 8 rutas internas tiene explicación
concreta: **no existen `netlify.toml` ni `public/_redirects`** en el
repositorio. Falta la regla de reescritura de SPA. Es un archivo de dos líneas.

**Qué NO se compiló.** El clon es superficial: **un solo commit, sin historial,
ramas, PRs ni issues** — así que no hay delta de commits ni decisiones
rescatadas de PRs cerrados, que es de donde el método dice que entra lo bueno de
un repo. No se leyó el contenido de los archivos salvo por búsquedas dirigidas,
ni se compiló ni se corrió nada. Miro y Figma siguen cerrados: **2 de 5 fuentes
sin acceso**. Los otros tres frentes siguen sin compilar a propósito.

**Fidelidad.** Todo de originales. Pero «original» resultó tener tres capas con
tres relojes distintos, y ésa es la lección de hoy.

**Conexiones entre frentes: ninguna que pase la vara, y se dice.** Sigue habiendo
un solo frente compilado; de los otros tres solo hay títulos. El candidato
—*el informe de resultados es falso y eso es un riesgo comercial*— tiene los dos
lados en la misma fuente, así que es contradicción interna (R1), no conexión.

**Qué queda marcado para quien decide.** Tres, por urgencia:

1. **El informe de resultados es de mentira y está en producción.** Todo usuario
   ve 6.4. Es lo que se rompe solo en una demo.
2. **El despliegue está atrasado respecto del repositorio.** Se está demostrando
   menos producto del que existe.
3. **Faltan `netlify.toml` o `public/_redirects`** y por eso el sitio da 404 en
   cualquier enlace directo.


## 2026-09-17 — Arranque del vault y compilada piloto del frente Entrevista

**Qué se compiló.** Se creó el vault con `cerebro init` (4 frentes, 3 skills) y
se compiló **un solo frente**, Entrevista, como manda el paso 2 del arranque.
Producto: `proyectos/entrevista.md` con los ocho bloques vivos, 9 numeralias
fechadas y citadas, 4 contradicciones y 4 riesgos. `cerebro verificar` cierra en
**0 errores**.

**Qué NO se compiló, y por qué.**

- **Universo de fuentes: 4 contenedores. Leídos: 2.** Miro y Figma quedaron
  fuera **por falta de permiso, no por criterio** — es lo que más pesa de esta
  corrida. Mientras sigan cerrados, toda compilada de este vault es parcial por
  construcción, y el diseño, que es donde suele vivir la decisión de producto,
  no entra.
- **Tres de los cuatro frentes quedaron sin compilar a propósito:** Vacantes,
  Comercial e Incubación. No es un hueco, es el paso 2 del arranque — escalar
  antes de auditar el piloto multiplica por cuatro cualquier regla mala.
- **Notion: 17 de 17 filas abiertas, pero solo 3 tienen cuerpo.** Las otras 14
  están en blanco, incluidas *todas* las de Bussiness y Producto. Lo que se sabe
  de esos frentes viene **únicamente de títulos**, y un título no es una fuente.
- **Sitio: nunca se vio renderizado ni autenticado.** Es una SPA que WebFetch no
  ejecuta, y sus 8 rutas internas devuelven 404. Lo leído salió del **bundle
  compilado**. Nada de lo que hay detrás del login se compiló.
- **Sin leer y es material:** los dos diagramas embebidos desde Figma dentro de
  *Stack Tecnologico*; las secciones 6 a 12 de esa página, que no aparecen en el
  render público — el documento salta de «5. Base de datos» a «13. Registro», y
  **no sé si están ocultas o nunca se escribieron**; comentarios e historial de
  versiones de Notion.

**Medición de propiedades, antes de confiar en ellas.** El tablero se agrupa por
`Priority`, que cubre **14 de 17** filas. La columna de estado dice *Not started*
en **17 de 17** — 0% de señal: no refleja que tres páginas ya tienen trabajo
escrito ni que una se editó el mismo día. **Ninguna de las dos describe el
avance.** Se agrupó por contenido.

**Fidelidad.** Todo salió de originales —tablero y código—, **nada de
resúmenes**. Pero con una salvedad que hay que repetir cada vez que se cite esta
nota: «original» aquí significa *el código escrito*, no *el sistema corriendo*.
Ninguna cifra de esta compilada ha salido del vault, y ninguna debe salir sin
verificarse contra el original.

**Contradicciones nuevas: 4.** C1 la voz (documentada y prometida, ausente del
bundle) · C2 la evaluación (rúbrica de 7 dimensiones contra un 6.4 fijo para
todo usuario) · C3 la infraestructura (Cloudflare contra Netlify; 6 tablas
contra 5 con otros nombres) · C4 las vacantes (pipeline completo en Notion, sin
rastro en el sitio). **Las cuatro quedan registradas, ninguna resuelta.** Hay
una hipótesis que las reconcilia —Notion es el objetivo, el sitio es el estado—
y está escrita **como hipótesis**, porque ninguna fuente lo dice.

**Conexiones entre frentes: ninguna que pase la vara, y se dice.** El barrido
corrió. El candidato más fuerte fue *la portada promete voz y contratación en
dos semanas mientras el producto escribe y devuelve un puntaje fijo*, que tiene
consecuencia comercial clara. **No entra como conexión** porque falla la segunda
condición: los dos lados salen de **la misma fuente**, el bundle. Eso no es una
conexión entre Comercial y Entrevista — es una contradicción dentro de
Entrevista, y ahí quedó registrada como R1. La razón de fondo de que no haya
conexiones es medible: solo hay un frente compilado, y de los otros tres solo
tengo títulos. Inventar una conexión débil vale menos que declarar que no hubo.

**Qué queda marcado para quien decide.** Cinco cosas, por urgencia:

1. **¿Notion es el plan de diciembre o el estado de hoy?** Una frase cierra las
   cuatro contradicciones o las convierte en deuda de producto.
2. **El sitio está roto para cualquier enlace directo**: 8 de 8 rutas internas
   dan 404 por falta de la regla de reescritura de SPA. Es el arreglo más barato
   de toda la lista.
3. **La portada promete lo que el producto no hace.** El riesgo no es técnico:
   es una demo en vivo delante de la contraparte o de un comprador.
4. **Abrir Miro y Figma.** Dos de cuatro fuentes cerradas. Ojo con el tope de 20
   lecturas al mes del plan actual de Figma: ya se gastaron 4.
5. **Llenar los 11 blancos de `CLAUDE.md`** — quién eres, dónde te atoras, y las
   metas. **No hay meta comprometida en ninguna fuente leída**, y hasta que la
   haya el vault registra actividad pero no puede responder *"¿voy bien?"*.

**Qué revisar y con qué comando.** Todo está sin commitear del lado tuyo por
diseño; lo que dejó esta corrida se lee con:

```
git diff --stat HEAD~1
cerebro verificar
```


<!-- Plantilla de una entrada:

## AAAA-MM-DD — Título de la corrida

**Qué se compiló.** Fuentes leídas, notas tocadas, con números.

**Qué NO se compiló, y por qué.** El universo, cuánto quedó fuera y el criterio.
Una cobertura parcial que no se declara se lee como completa.

**Fidelidad.** Qué se leyó del original y qué de un resumen. Toda cifra que
venga de un resumen se marca en la nota.

**Hallazgos.** Máximo cinco, por urgencia, cada uno con su cifra y su cita.

**Contradicciones nuevas.** Numeradas siguiendo las existentes.

**Conexiones entre frentes.** Las que pasaron la vara de tres condiciones. Si
no hubo ninguna, se dice — vale más que inventar una débil.

**Qué necesito de ti.** En una línea.
-->
