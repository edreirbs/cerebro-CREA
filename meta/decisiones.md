# Decisiones del sistema

Registro de cómo se opera este vault y por qué. **Se agrega, no se reescribe.**

Formato de cada entrada: la fecha, qué se decidió, **Por qué**, **Cómo se
aplica**, y **qué alternativa se descartó**. Si una decisión corrige a otra
anterior, se dice cuál.

> Este archivo es la pieza más valiosa del sistema y la más fácil de saltarse.
> Una regla sin su error se lee como burocracia y se incumple; con su error, se
> obedece.

---

# Heredadas del método

Estas no las pagó este vault: vienen destiladas de dos vaults anteriores que se
equivocaron primero. Están aquí para no volver a pagarlas.

**Se pueden cambiar** — pero cambiarlas es una decisión que se escribe abajo,
con su fecha y su porqué, no una que se toma en silencio.

## ⬅ Lista blanca en vez de lista negra
El vault solo acepta contenido de los frentes declarados. **Por qué:** la
alternativa —aceptar todo y etiquetar lo sensible— se probó y falla, porque una
etiqueta es un rótulo, no un candado. **Descartada:** aceptar todo con
etiquetas.

## ⬅ Un tema = un archivo, y la nota de proyecto tiene anatomía fija
N fuentes producen **una** nota actualizada con N citas. **Por qué:** dos notas
sobre lo mismo se desincronizan a la primera actualización, y entonces hay dos
versiones del mismo hecho y ninguna manda.

## ⬅ Una entidad con varios nombres produce una nota y varios alias
**Cómo decidir si son la misma cosa:** ¿usuarios propios, dueño propio y
presupuesto propio? Si las tres son sí, son notas separadas; si las tres son no,
es una nota con alias de una pantalla. **El nombre no decide nada**: decide a
quién sirve, quién responde y de qué bolsa sale. **Descartada:** una nota
completa por cada nombre — produce tres versiones del mismo hecho.

## ⬅ La ficha en `fuentes/` se reserva
Hay ficha solo si la fuente es un **original no recuperable**, o si —sin ser
minuta— **sostiene una cifra o decisión citada**. Lo que se abre con un clic
lleva línea de cita con URL. **Por qué:** la versión ingenua ("cada fuente tiene
ficha") produjo **54 fichas de un solo proyecto**; al corregir quedaron 6 y no
se perdió ni un hecho. **Y el contraejemplo:** en el otro vault esta regla nunca
se escribió y la carpeta quedó vacía tres semanas.

## ⬅ Una compilada parcial se declara parcial, con números
Sección `## Cobertura de esta compilada` con el tamaño del universo, cuánto se
compiló, el criterio de selección, y qué quedó fuera. **Por qué:** una nota bien
escrita se lee como completa aunque no lo sea, y ésa es la manera en que una
cifra faltante llega a una presentación.

## ⬅ Una afirmación de ausencia se escribe como "no encontré, buscando así"
Nunca como "no existe". **Por qué:** una ausencia es lo más fácil de escribir
mal porque **no falla ruidosamente** — basta con no haber buscado bien. Un vault
real escribió tres cifras negativas en una pasada y el reconteo desmintió las
tres; una ya se había propagado a otras tres notas.

## ⬅ Contradicción de cifra o de compromiso: se registran las dos, no se elige
**No se promedia, no se elige la más reciente, no se elige la más conservadora.
Se pregunta.** Si existe una lectura que las reconcilie, se escribe **marcada
como hipótesis**, nunca como hecho.

## ⬅ Las contradicciones viven en sección propia, separadas de los riesgos
Un riesgo es algo que puede pasar; una contradicción es algo que **ya está mal
en el expediente**. Mezclarlas hace que las contradicciones se lean como
preocupaciones en vez de como pendientes.

## ⬅ Toda cifra que salga del vault se verifica contra el original
Dentro del vault, un resumen basta para saber por dónde va algo. Fuera —una
presentación, un correo, una junta— **la cifra lleva tu nombre encima**. Y toda
cifra que sustente un juicio se mide **dos veces, con métodos distintos**, y la
nota dice **con qué** se midió.

## ⬅ Una extracción vacía es una hipótesis sobre el extractor
No un hecho sobre el documento. Antes de escribir "la cifra no está", verificar
**qué partes del archivo se leyeron** y decir cuáles no.

## ⬅ El archivo sin sufijo de versión es el bueno
Un "v2" o "v3" es borrador o variante: se puede leer, se puede registrar que
difiere, **y no se cita para reportar**. **Por qué:** leer el archivo equivocado
produjo la conclusión —falsa— de que tres metas habían desaparecido.

## ⬅ Una versión nueva se difiere contra la anterior, no la sustituye
**Lo que desaparece de una versión a otra es tan informativo como lo que se
agrega.** Un documento real retiró dos limitaciones declaradas sin agregar dato
nuevo, contradiciendo lo que su autor ya había sostenido en público.

## ⬅ Cerrar una contradicción obliga a cerrarla en TODAS las capas
Y reabrirla obliga a reabrirla en todas. **Por qué:** las capas envejecen a
distinta velocidad — la nota se reescribe cada compilada, la bitácora es
histórica, los resúmenes se actualizan solo si alguien se acuerda. **Corolario:**
antes de declarar que el vault tenía un dato mal, localiza **en qué capa** estaba
el error. Un resumen comprime, y al comprimir pierde distinciones.

## ⬅ Una propiedad que agrupa bien en un frente no agrupa bien en todos
Empezar por la etiqueta, **verificar su cobertura contra el contenido**, y
agrupar por contenido si no cubre. **Por qué:** una propiedad que etiquetaba
bien dos proyectos etiquetaba **14 de ~140 documentos** en un tercero. Confiar en
ella habría producido una nota afirmando que ese proyecto llevaba un año
detenido.

## ⬅ El agente compila; la persona commitea
La corrida automática escribe notas y **no hace commit**. **Por qué:** la
revisión humana queda forzada por diseño; nada entra al historial sin que
alguien lo haya visto. Toda corrida que deje cambios entrega **qué revisar y el
comando exacto**.

## ⬅ Ficha en `personas/` solo para quien bloquea, decide, o se repite
Los demás quedan como texto dentro de la nota. **Por qué:** una ficha por cada
nombre convierte la carpeta en un directorio telefónico. Una oleada real levantó
más de sesenta nombres propios; con la regla ingenua habrían sido sesenta
archivos que nadie releería.

## ⬅ El contenido y la cuenta deben coincidir
Trabajo de una organización en infraestructura de esa organización; trabajo
propio en cuenta propia. **Si algo podría ir en los dos, no va en ninguno hasta
preguntar.** **Y la lección de vigilancia:** la regla existía desde el día uno y
aun así un correo institucional terminó firmando commits publicados de un
proyecto personal — porque el repositorio nació **después** de que se escribiera
la lista de repos a vigilar. **Vigilar una lista no sirve; hay que vigilar el
momento en que algo se crea.**

## ⬅ Una carpeta con volumen anómalo se abre un nivel más antes de resumirla
**Por qué:** un cliente real, con trabajo entregado, vivía anidado dentro de la
carpeta de otro cliente y fue invisible dos compiladas seguidas. Un elemento
colgado de otro **hace que el conteo del padre mienta**.

## ⬅ Los correos no son fuente
Un correo es correspondencia, no documentación: trae cadenas de reenvío,
terceros que no consintieron aparecer, y contexto que se pierde al recortarlo.
**El hecho puede entrar; el correo no** — se busca ese hecho en una fuente
citable, o se confirma con quien sabe y se registra como *"confirmado por X,
fecha"*.
> 🟡 Ésta es la más discutible de las heredadas. Si en tu caso el correo **es**
> el registro formal, cámbiala aquí abajo con tu razón.

## ⬅ El barrido de conexiones corre aunque no haya material nuevo
Las conexiones no salen de lo nuevo: salen de releer lo viejo junto. **La vara:**
una conexión entra si cumple las tres — no es obvia leyendo un solo frente,
cita textualmente los dos lados, y tiene una consecuencia accionable. **Si una
vuelta no produjo ninguna, se dice.**

---

# Decisiones de este vault

> A partir de aquí, las tuyas. La primera suele salir del alto después del
> piloto — ver `ARRANQUE.md`, paso 3.

## 2026-09-17 — El universo de fuentes se barre; no se acepta la lista que te dan
**Qué pasó, y pasó dos veces el mismo día.** Se escribió *"la voz no está
construida"* y *"el pipeline de vacantes es plan puro"*. Las dos eran falsas. La
voz estaba en el repositorio; las vacantes estaban **desplegadas** como un
producto llamado «Radar Laboral», que apareció solo al listar los 8 proyectos de
la cuenta de Netlify en vez de mirar el enlace recibido.
**Por qué importa.** Las dos veces el error tuvo la misma forma: **el universo
examinado era el de los enlaces que llegaron**, y una ausencia dentro de un
universo mal delimitado no dice nada sobre el mundo. Es el mismo error que el
método ya registra con otras palabras — *vigilar una lista no sirve; hay que
vigilar el momento en que algo se crea* — y aquí costó dos afirmaciones falsas
antes de verse.
**Cómo se aplica.** Antes de escribir cualquier ausencia se **enumera el
contenedor completo**: los repos de la cuenta, los despliegues del equipo, los
proyectos del espacio. Y la nota declara **cuántos se enumeraron**, no solo
cuántos se leyeron. Un enlace recibido es un punto de entrada, nunca el universo.
**Descartada:** confiar en que las fuentes entregadas estaban completas. Es
cómodo y es exactamente lo que falló.
**Corrige a:** la regla de hoy sobre *repositorio → despliegue → Notion*, que
ordenaba bien las capas pero daba por buena la lista de objetos dentro de cada una.

## 2026-09-17 — El repositorio es la fuente primaria del producto; el despliegue no
**Qué pasó.** La primera compilada concluyó que la entrevista por voz *"no
estaba construida"*, con evidencia que parecía dura: cero ocurrencias de
`getUserMedia`, `MediaRecorder` y `AudioContext` en el bundle desplegado. Al
abrir el repositorio, las tres estaban ahí, más un componente de voz completo y
una edge function de transcripción. **La afirmación era falsa.**
**Por qué importa.** El error no estuvo en el dato sino en **qué capa se leyó**.
Un bundle desplegado es una foto vieja del código, y una búsqueda vacía sobre él
es *una hipótesis sobre el despliegue*, no un hecho sobre el producto. Es
exactamente el modo de fallo que el método señala: una afirmación de ausencia no
falla ruidosamente — basta con no haber buscado donde había que buscar.
**Cómo se aplica.** Toda afirmación sobre lo que el producto hace o no hace se
verifica **contra el repositorio**, y se dice en qué capa se verificó. Orden de
autoridad, de mayor a menor: **repositorio → despliegue → Notion**. Una ausencia
solo se escribe después de buscarla en el repositorio, y se escribe *"no
encontré, buscando así"*.
**Descartada:** tratar las tres capas como una sola fuente, que fue justo lo que
produjo el error. Son tres relojes distintos y hay que fecharlos por separado.

## 2026-09-17 — CREA es un cerebro aparte, no una carpeta del personal ni del Tec
**Por qué:** el método exige que el contenido y la cuenta coincidan, y lo exige
como **dos vaults separados, no dos carpetas del mismo**. CREA no es trabajo
personal ni institucional: es una tercera cosa con su propia ventana
(jun–dic 2026) y su propia contraparte.
**Cómo se aplica:** este repositorio solo acepta material de los cuatro frentes
de CREA. Lo personal y lo del Tec no entran aquí ni siquiera "temporalmente".
**Descartada:** una carpeta `crea/` dentro del cerebro que ya existe — habría
mezclado dos calendarios, dos contrapartes y dos criterios de qué es urgente.

## 2026-09-17 — La lista blanca son cuatro frentes: entrevista, vacantes, comercial, incubacion
**Por qué:** cada uno pasa las tres preguntas del método —usuarios propios,
dueño propio, presupuesto propio—. *Entrevista* consume audio y tokens por
sesión y tiene tabla `Usage` dedicada; *Vacantes* gasta cuotas de proveedores
externos y sirve a quien busca empleo, no a quien practica; *Comercial* le vende
a una organización, no al candidato; *Incubación* tiene calendario propio.
**Cómo se aplica:** lo que no encaje en uno de los cuatro se reporta en la
bitácora y se deja donde está.
**Descartada — y ésta es la que importa:** *Producto / experiencia* como quinto
frente, que en el tablero de Notion aparece agrupado como si lo fuera. No pasa
la prueba: sus usuarios son los mismos que los de *Entrevista* y no tiene
presupuesto propio. Es una **dimensión** de un frente, no un frente. Convertirla
en uno habría producido dos notas que se desincronizan sobre el mismo producto.
**También descartada:** un solo frente «EntrevistIA» para todo. Habría metido
la venta B2B y el compromiso con el programa de incubación en la misma nota que
el motor de entrevista, y ésa es exactamente la nota que crece hasta que deja de
responder en segundos.

## 2026-09-17 — `publica: "contenido"`, y se elige por seguridad, no por publicar
**Por qué:** ese interruptor decide si los cuerpos salen del vault, y es **el
mismo** que enciende el chequeo de fugas de `cerebro verificar`. Medido sobre
una nota de prueba con datos ficticios: con `"metadatos"` una matrícula y un
correo pasaron con **0 errores**; con `"contenido"` los dos se reportaron como
error que nunca baja a advertencia.
**Cómo se aplica:** queda encendido desde ahora, mucho antes de que exista
cualquier publicación real.
**Descartada:** dejar `"metadatos"` hasta que hubiera algo que publicar. Habría
dejado el chequeo apagado justo durante los meses en que se escriben las notas.
**Y su límite, medido el mismo día:** el chequeo **no** detecta nombres de
personas ni teléfonos. Para un vault cuyo bloque de compromisos ajenos *son*
nombres, eso significa que la protección real es la regla del semáforo, no el
programa.

## 2026-09-17 — Un enlace de invitación es una credencial y no se versiona
**Por qué:** el enlace de Miro que abre este vault es del tipo que da entrada a
un **equipo**, no solo a un tablero. Guardarlo en un archivo versionado lo
publica de facto: lo que se commitea queda en el historial aunque después se
borre el archivo.
**Cómo se aplica:** en `cerebro.json` se nombra el contenedor y se anota que no
hay acceso. El enlace vive fuera del vault.
**Descartada:** guardarlo "por comodidad" en la configuración, que es como
empiezan todas las filtraciones de este tipo.

## 2026-09-17 — La identidad de git es local a este repositorio, nunca global
**Por qué:** una identidad global firma en silencio lo que sea que se cree
después, y el autor de un commit no se corrige moviéndolo — hay que reescribir
el historial. El caso que produjo la regla: un correo institucional terminó
firmando commits ya publicados de un proyecto personal.
**Cómo se aplica:** `git config --local user.email`. Este repositorio arrancó
firmado por el agente a propósito, **no** con el correo institucional de la
sesión, que no corresponde a CREA.
**Descartada:** usar el correo institucional disponible. Es precisamente el
cruce que la regla prohíbe.

---

# Decisiones abiertas

> Lo que está decidido a medias. Vivir con una pregunta abierta y escrita es
> mucho mejor que cerrarla en silencio con una suposición.

## ~~¿Lo que Notion describe es el plan de diciembre o lo que ya existe?~~ — CERRADA 2026-09-17
**Respuesta: mixta, y ahora medible contra el repositorio.** La voz ya se
construyó (Notion tenía razón); la evaluación por rúbrica y el pipeline de
vacantes siguen siendo plan; y la infraestructura que Notion describe —Cloudflare,
6 tablas— **no es la que se construyó** (Supabase Edge Functions, 4 tablas): ahí
el error es de Notion. Queda el detalle abajo por valor histórico.

<!-- Planteamiento original:
De esto dependen las cuatro contradicciones C1–C4 de
`proyectos/entrevista.md`: si Notion es el objetivo del sprint, son deuda de
producto y el expediente está bien; si Notion describe el presente, el
expediente está mal y hay que corregirlo. **Hay una hipótesis que reconcilia
las cuatro —Notion es el objetivo, el sitio es el estado— pero ninguna fuente
la dice, así que queda marcada como hipótesis y no como hecho.**
**Quién la cierra:** quien decide. Una frase basta. -->

## ¿«Radar Laboral» es parte de EntrevistIA o un producto hermano?
Hallado el 2026-09-17 en la cuenta de Netlify (`jobinderai.netlify.app`). Hace
lo que el *Scrapper* de Notion describe, pero **vive fuera del repositorio de
EntrevistIA y en una cuenta de Netlify distinta de la que sirve el sitio de
EntrevistIA**. De la respuesta depende la lista blanca: si es parte, `vacantes`
es un frente de un producto; si es hermano, la pregunta de si CREA es una
incubadora con varios proyectos ya se contestó sola, y los frentes tendrían que
ser los proyectos.
**Hueco pendiente:** qué bolsas de trabajo usa. El pipeline corre del lado
servidor detrás de `/api/recommendations`; no se ve desde el navegador. Se
resuelve con acceso a su repositorio.
**Quién la cierra:** quien decide. Mientras siga abierta, `vacantes` no se
compila.

## ¿CREA es EntrevistIA, o es una incubadora con varios proyectos?
La base de Notion se llama *Incubadora de proyectos*, en plural, pero todo su
contenido es de un solo producto. Si mañana entra un segundo proyecto, la lista
blanca de cuatro frentes deja de servir: los frentes serían los proyectos, no
las partes de éste. **Mientras siga siendo uno, la lista actual es correcta.**
Es una decisión que hay que reabrir el día que aparezca el segundo, no antes.

## ¿Con qué correo se firman los commits de CREA?
Hoy firma el agente. CREA es trabajo propio en cuenta propia, así que le toca
un correo personal — no el institucional de la sesión. Un comando lo cierra:
`git config --local user.email "..."`.

## ¿Cómo se abren Miro y Figma?
Dos de las cuatro fuentes están cerradas, y mientras sigan así **toda compilada
de este vault es parcial por construcción**. Figma pide que el dueño comparta el
archivo con rol de editor o lo mueva a un plan donde la cuenta tenga asiento;
Miro pide aceptar la invitación al equipo desde un navegador con sesión. Ojo:
el plan actual de Figma tiene tope de **20 lecturas al mes** y ya se gastaron 4
en los intentos del 2026-09-17.

---

# Diferido, con su razón

> Lo que se evaluó y se pospuso a propósito, para no volver a discutirlo cada
> mes.

## Publicar el cerebro y dejar que lectores le pregunten al modelo
**Se quiere**, y está decidido. **No se puede todavía:** el kit instalado no
implementa esa ruta — no existen `cerebro publicar` ni `cerebro construir`, ni
la función que responde preguntas. Es el paso 7 del arranque, no el día uno.
Cuando llegue el momento, el orden de `INSTALAR.md` tiene un paso que no se
puede invertir: **el límite de gasto mensual va antes de generar la API key**;
si la llave se filtra antes de que exista el límite, no hay techo. Y esa cuenta
es independiente de la suscripción: la suscripción no cubre lo que gasten los
lectores.

## Fichas en `personas/`
Vacío a propósito. La compilada del 2026-09-17 no levantó ni un nombre por la
regla de datos personales, y con `publica: "contenido"` encendido cada nombre
que entre va a salir publicado. Se abre cuando haya una decisión explícita sobre
qué nombres pueden salir.
