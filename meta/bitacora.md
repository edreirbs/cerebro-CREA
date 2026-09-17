# Bitácora

Qué se compiló, **qué no se compiló y por qué**, y qué quedó marcado para
revisar. Se agrega arriba: lo más reciente primero.

> Esto es un cuaderno de laboratorio, no un changelog. Los errores propios se
> registran con la misma prominencia que los aciertos — son los que producen las
> reglas de `meta/decisiones.md`.

> Cuando pase de unas 600 líneas, se corta por año a `meta/bitacora/<año>.md`.
> La compilada solo lee las últimas tres entradas; el resto es histórico.

---

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
