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

## 2026-09-17 — Auditoría del piloto: la capa meta pesa 3.7× más que el conocimiento
**Qué se midió** (paso 3 del arranque, las tres preguntas):

1. **¿Cuántos archivos produjo?** Seis, pero **una sola nota de conocimiento**:
   `proyectos/entrevista.md`, 202 líneas. Contra ella, la capa meta suma **759**
   —`decisiones.md` 473 y `bitacora.md` 286—. **Proporción 3.7 a 1 a favor del
   vault hablando de sí mismo.**
2. **¿Cuántos se van a releer?** `entrevista.md` sí, en cada junta. `CLAUDE.md`
   se carga solo. De `bitacora.md` se leen **las últimas tres entradas**, por
   diseño. De `decisiones.md`, **13 entradas escritas en un solo día, nadie las
   va a releer completas**, y ése es exactamente el defecto que el método
   registra con las 54 fichas: producir material que envejece sin relectura.
3. **¿Qué regla resultó falsa al tocar material real?** **Tres**, y todas mías:
   que el despliegue refleja el producto · que el universo de fuentes es el que
   te entregan · que un bloqueo de acceso significa falta de permiso.

**El diagnóstico, que es peor que las tres fallas sueltas.** Las tres son **la
misma**: afirmé sin verificar en qué capa estaba mirando, y cada una se corrigió
solo cuando llegó evidencia nueva o cuando alguien me cuestionó. **El ciclo
corrió al revés:** compilar → publicar → que me corrijan, en vez de verificar →
compilar. Y produjo su propio síntoma: **3 de las 5 entradas de bitácora del día
son correcciones de errores propios**, no compiladas.

**La regla, una en vez de tres.** Antes de escribir una afirmación de ausencia
—*no existe, no está construido, no hay acceso*— se hace **una verificación más,
en otra capa**, y esa verificación se cita en la nota. Sin segunda capa, no se
escribe la ausencia: se escribe el hueco. Las tres entradas previas de hoy sobre
capas, universo y acceso son **casos** de ésta, no reglas independientes.

**Cómo se aplica al tamaño.** No se borra nada —`decisiones.md` se agrega, no se
reescribe— pero **se deja de escribir una entrada por incidente**. Una entrada
nueva solo si la lección no está ya cubierta por una existente; si lo está, se
anota como caso bajo ella. Y **si a la siguiente compilada la proporción no se
ha invertido, el problema no es el registro: es que el vault no está compilando
conocimiento.**

**Descartada:** podar `decisiones.md` ahora. Tiene un día de vida: podar lo que
todavía no se ha releído es adivinar qué sobra. Se revisa en la compilada que
cierre el mes.

## 2026-09-17 — CREA es una organización incubadora, no un producto
**Qué se decidió.** CREA *"idea, desarrolla, incuba y despliega ágilmente casos
de negocio basados en tecnologías digitales e IA"*. Es la casa, no el producto.
**Por qué importa.** Confirma que la lista blanca actual —cuatro partes de
EntrevistIA— **es correcta hoy y caduca sola**: si CREA incuba casos, el día que
entre un segundo caso los frentes dejan de ser las partes de uno y pasan a ser
los casos. La base de Notion ya se llama *Incubadora de proyectos*, en plural.
**Cómo se aplica — el disparador, escrito para no depender de que alguien se
acuerde:** en cuanto aparezca material de un segundo caso de negocio, **no se
compila a ningún frente existente**: se detiene y se rehace la lista blanca.
Compilarlo dentro de `entrevista` sería meter dos productos en una nota, que es
el modo de fallo que el método llama *un tema, un archivo*.
**Descartada:** rehacer la lista blanca ahora, por frentes tipo *ideación ·
desarrollo · incubación · despliegue*. Ésas son **etapas de un pipeline**, no
frentes: comparten usuarios y presupuesto, y ninguna responde *"¿cómo va X?"*.

## 2026-09-17 — No se escriben los dolores ni la meta, y se declara qué cuesta
**Qué se decidió.** Quien opera el vault decidió no llenar por ahora la tabla de
*dónde me atoro* ni las metas comprometidas.
**Por qué se registra en vez de dejarlo en blanco.** Un blanco de plantilla se
lee como trabajo pendiente; **esto es una decisión**, y la diferencia es que
trae su costo escrito. Sin dolores, el vault compila todo con la misma urgencia
y no puede ordenar sus hallazgos por lo que destraba a quien lo lee. Sin meta,
responde *"¿qué pasó?"* pero **no "¿voy bien?"** — no hay contra qué medir.
**Cómo se aplica.** Las dos secciones dicen explícitamente que están vacías por
decisión y qué se pierde. Se llenan cuando se quiera; el efecto es inmediato y
no hay que migrar nada.
**Descartada:** inventar metas a partir de los objetivos técnicos de desempeño
que sí aparecen en Notion. Dicen qué tan rápido carga la landing, no si el
negocio va bien, y usarlos como meta habría producido un vault que responde que
todo va bien midiendo lo que no importa.

## 2026-09-17 — «Tú tienes acceso» y «el conector tiene acceso» son cosas distintas
**Corrige a:** la decisión de hoy *«Un enlace no es un acceso»*, que tenía el
hecho bien —no se pudo leer— y **la causa mal**. Dijo que faltaba permiso. No
faltaba: estaba dado.
**Qué se midió, al ser cuestionada.** `whoami` de Figma devuelve la cuenta
**institucional `@tec.mx`**, que pertenece a **un solo plan** —el equipo personal
de esa cuenta, tier starter— y no al plan del archivo de CREA. Y el error de
lectura no dice *"no tienes acceso"*: dice ***"no tienes acceso de edición; el
dueño puede hacerte editor"***. Es decir, **el conector de Figma exige asiento de
editor; ser lector no alcanza**. En Miro, la cuenta del conector busca
«entrevist» entre sus tableros y devuelve **0 de 0**: el tablero no está en su
equipo.
**Por qué importa.** Es el mismo error de capa que ya costó dos veces hoy:
**atribuir a la fuente un fallo que era del lector**. Reportarle a alguien que
"no dio permiso" cuando sí lo dio quema crédito y no destraba nada — el remedio
real es otro y más específico.
**Cómo se aplica.** Todo bloqueo de acceso se reporta con **tres datos, no uno**:
con qué cuenta se intentó, qué nivel de permiso pedía la herramienta, y el error
textual. Sin los tres, no es un reporte: es una suposición.
**Remedio concreto de los dos:** en Figma, asiento de **editor** para la cuenta
del conector, o reconectar el conector con una cuenta que ya lo tenga. En Miro,
aceptar la invitación desde un navegador con sesión de **esa misma cuenta**.
**Descartada:** insistirle a la contraparte por "permiso de lectura". Ya estaba
dado; pedirlo otra vez no habría cambiado nada.
**Y una bandera aparte:** el conector de Figma corre con la cuenta `@tec.mx`.
Material de CREA —que no es del Tec— se estaría leyendo con infraestructura
institucional. Es el cruce que el método prohíbe. Ver la decisión sobre cuentas.

## 2026-09-17 — Un enlace no es un acceso: los tres bloqueos siguen abiertos
> ⚠️ **Corregida por la entrada de arriba:** el hecho es correcto, la causa no.
**Qué pasó.** Se asumió que con los enlaces entregados bastaba. **Medido: no
basta.** Figma devuelve *"Looks like you don't have edit access to this file"* en
las cuatro llamadas de lectura; Miro resuelve a una página de *unirse al equipo*
y su API no ve ese tablero entre los 74 de la cuenta; y el sitio de EntrevistIA
no está entre los 8 proyectos de la cuenta de Netlify conectada.
**Por qué importa.** Un enlace es una dirección; el acceso es un permiso que da
otra persona. Confundirlos deja al vault **declarando cobertura completa sobre
un universo que no pudo abrir** — y una compilada parcial que no se declara se
lee como completa.
**Cómo se aplica.** Los tres viven como **compromisos ajenos con fecha de
apertura** en `proyectos/entrevista.md`, no como pendientes técnicos. Cada
compilada reintenta y actualiza su antigüedad. Y toda nota de este frente
declara que **dos de sus fuentes nunca se han leído**.
**Descartada:** reintentar a ciegas. El plan de Figma tiene tope de 20 lecturas
al mes y ya se gastaron 4 sin obtener nada.

## 2026-09-17 — Las fuentes de CREA son ajenas, y entran igual
**Qué se decidió.** El repositorio, Notion, Miro y Figma pertenecen a otras
personas. **Entran como fuentes de todas formas.** La lista blanca filtra por
**tema**, no por propiedad: nunca pidió que las fuentes fueran de uno.
**Por qué importa, y es lo que no se ve de entrada.** Cambia dos cosas del
método para este vault:

1. **Los bloqueos de acceso son compromisos ajenos, no pendientes tuyos.** Miro
   y Figma no se arreglan con esfuerzo propio: alguien más tiene que dar
   entrada. Por eso viven en el bloque *Compromisos ajenos* de
   `proyectos/entrevista.md`, con su fecha de apertura, y envejecen a la vista
   como cualquier otro compromiso — que es justo lo que los hace accionables.
2. **«Se abre con un clic» deja de ser garantía.** El método reserva la ficha en
   `fuentes/` para el original irrecuperable, porque lo consultable se cita con
   su URL en vez de copiarse. Con fuentes ajenas esa garantía es de otro: el
   sitio público de Notion se despublica con un clic ajeno, y el acceso al repo
   se revoca igual. **Recalibración:** cuando una fuente ajena sostenga una
   cifra o una decisión que se vaya a citar, se levanta ficha en `fuentes/` con
   lo destilado y su fecha de lectura, aunque hoy se abra con un clic.
**Cómo se aplica.** Nada cambia en la lista blanca ni en la configuración. Lo
que cambia es el criterio de ficha, arriba, y que las tres fuentes cerradas se
reportan como compromisos ajenos con antigüedad.
**Descartada:** exigir propiedad o acceso garantizado antes de declarar una
fuente. Habría dejado fuera **todo** el material de CREA — el universo entero es
ajeno — y un vault sin fuentes no compila nada.
**Lo que NO cambia:** que este repositorio, el cerebro, sí es tuyo y vive en tu
cuenta. Es el contenedor de lo destilado, no de los originales.

## 2026-09-17 — El producto de vacantes hallado en Netlify NO entra: es el primer rechazo del vault
**Qué se decidió.** El producto desplegado que apareció al enumerar la cuenta de
Netlify —parecido al *Scrapper* que Notion documenta— **queda fuera de este
vault** por decisión de quien decide. No es de CREA.
**Por qué importa más de lo que parece.** Es la primera vez que este vault
**rechaza**, y rechazar es literalmente su razón de ser: un vault que acepta
todo lo que se parece a sus frentes es un archivero en seis semanas. El parecido
temático no es pertenencia — lo que decide es a quién sirve, quién responde por
ello y de qué bolsa sale, y la respuesta fue que no es CREA.
**Cómo se aplica.** Se saca de la lista blanca, de la configuración y de la nota
de proyecto. **No se borra de la bitácora**: haberlo encontrado y haberlo
rechazado es historia del vault, y la bitácora es cuaderno de laboratorio, no
changelog. Se nombra sin enlace ni detalle — *se reporta y se deja donde está*.
**Y la consecuencia sobre el frente `vacantes`:** vuelve a ser **plan, no
producto**. Hoy existe como documento de Notion y nada más.
**Descartada:** meterlo como quinto frente o como parte de `vacantes` por
parecido temático. Habría contaminado la lista blanca con algo ajeno, que es
exactamente el modo de fallo contra el que el método escribe la regla.
**Corrige a:** la compilada del 2026-09-17 (3), que lo dio por parte del frente
`vacantes` sin haber preguntado. **El error fue mío y de forma conocida:** eso
era rojo del semáforo —decidir la pertenencia de algo nuevo a un frente— y lo
traté como amarillo.

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

## ~~¿El producto de vacantes hallado en Netlify es parte de EntrevistIA?~~ — CERRADA 2026-09-17
**No lo es.** Queda fuera del vault; ver la decisión de arriba. Lo que sigue es
el planteamiento original, conservado porque la pregunta era correcta aunque la
suposición no.

<!--
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
compila. -->

## ~~¿CREA es EntrevistIA, o es una incubadora con varios proyectos?~~ — CERRADA 2026-09-17
**Es una incubadora.** Ver la decisión de arriba y su disparador. Planteamiento
original abajo.

<!-- ORIGINAL:
La base de Notion se llama *Incubadora de proyectos*, en plural, pero todo su
contenido es de un solo producto. Si mañana entra un segundo proyecto, la lista
blanca de cuatro frentes deja de servir: los frentes serían los proyectos, no
las partes de éste. **Mientras siga siendo uno, la lista actual es correcta.**
Es una decisión que hay que reabrir el día que aparezca el segundo, no antes. -->

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
