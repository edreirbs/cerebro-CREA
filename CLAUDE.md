# CLAUDE.md — CREA

> Este archivo es el mapa del vault. Se carga solo al iniciar cada sesión.
> Última actualización: 2026-09-17

> 🔴 **Contrato a medias.** Los frentes (§2) están cerrados y las fuentes (§11)
> verificadas. Lo que falta son los blancos `{{así}}`: quién eres, dónde te
> atoras y las metas. Es el paso 1 de `ARRANQUE.md` y es trabajo tuyo, no del
> agente — un dolor vago produce un vault vago. Búscalos con:
> `grep -n '{{' CLAUDE.md`

---

## 1. Quién soy y qué se espera de mí

{{QUIEN_ERES}}

- Reporto a: {{A_QUIEN_REPORTAS}}  *(el programa de incubación CREA tiene una
  contraparte; nómbrala por rol aquí)*
- Lo que esa persona espera de mí: {{QUE_ESPERAN}}
- Un día normal me trae: {{QUE_TE_LLEGA}}

**Esa expectativa es el propósito de este vault.** Todo lo que se compile aquí
debe servir para responder *"¿cómo va X?"* en segundos y con cita a la fuente.

### Dónde me atoro — lo que el vault tiene que resolver

Esta tabla es lo que separa un cerebro útil de un archivero bonito. Sé
específico: *"tengo mucha información"* no sirve; *"me piden el estado de todo
en una junta y tardo dos horas en juntarlo"* sí.

| Dolor | Qué hace el vault |
|---|---|
| {{DOLOR_1}} | {{COMO_LO_RESUELVE_1}} |
| {{DOLOR_2}} | {{COMO_LO_RESUELVE_2}} |
| {{DOLOR_3}} | {{COMO_LO_RESUELVE_3}} |

> Un dolor ya está medido y puedes copiarlo si te sirve: **lo que Notion dice
> que es el producto y lo que el sitio desplegado realmente hace no coinciden**,
> y nadie lo había puesto lado a lado. Está registrado en
> `proyectos/entrevista.md`.

---

## 2. Los frentes — lista blanca

Este vault **solo acepta contenido que pertenezca a uno de estos**. Si algo no
encaja en ninguno, **no entra**. No hay lista negra: lo que no está aquí queda
fuera por omisión.

El criterio con que se separaron —y lo que se descartó— está en
`meta/decisiones.md`, entrada del 2026-09-17.

### 1. Entrevista
El producto en vivo: el embudo registro → onboarding → entrevista → informe de
evaluación. Cuelga de aquí el motor de preguntas, la capa de voz (**ya
construida, no desplegada** — corregido 2026-09-17), la rúbrica de evaluación y
el consumo por sesión.
**Usuario propio:** el candidato que practica. **Presupuesto propio:** audio y
tokens por sesión.

### 2. Vacantes
El pipeline CV → perfil → proveedores de empleo → score → rerank, que en Notion
aparece como *Scrapper* y que **ya existe desplegado** como «Radar Laboral»
(`jobinderai.netlify.app`) — hallado el 2026-09-17, sin compilar todavía. **Usuario propio:** quien busca trabajo, que no es
necesariamente quien practica. **Presupuesto propio:** cuotas de proveedores
externos de vacantes más las llamadas de rerank.

### 3. Comercial
Venta y canal B2B: pitch, elevator pitch, estructura de la oferta a empresas e
instituciones. **Usuario propio:** la organización que compra, no el candidato.
**Presupuesto propio:** de venta, no de infraestructura.

### 4. Incubación
El programa CREA en sí: el sprint declarado **jun 2026 – dic 2026**, sus
entregables, sus hitos y los compromisos con la contraparte del programa.
**Usuario propio:** el programa. **Calendario propio**, que es lo que lo hace
separable de los otros tres.

**Lo que NO entra aquí, y dónde vive:** todo lo personal y todo lo del Tec.
Eso es otro cerebro, con su propio repositorio. Son **dos vaults separados, no
dos carpetas del mismo** — ver `meta/decisiones.md`.

---

## 3. Personas

Ficha en `personas/` **solo** para quien cumple al menos uno de tres criterios:
**bloquea** · **decide** · **se repite** (aparece en dos o más frentes). Los
demás quedan como texto dentro de la nota, citables y buscables, sin nodo en el
grafo.

| Persona | Rol | Qué necesito de esa persona |
|---|---|---|
| {{PERSONA_1}} | {{ROL}} | {{QUE_NECESITAS}} |

> Vacía a propósito: la compilada del 2026-09-17 no levantó ni un nombre, por
> la regla de no escribir datos personales. Dos huecos ya identificados piden
> una persona con nombre y rol: quién es dueño del archivo de Figma y quién
> administra el equipo de Miro. Ver `proyectos/entrevista.md`.

> 🎯 Si dos frentes distintos se traban con dos personas que reportan a la
> misma, esa tercera persona es tu palanca más eficiente. Anótalo aquí.

---

## 4. Metas y calendario

**Calendario:** jun 2026 – dic 2026, la ventana del sprint de incubación,
tomada de la descripción de la base de Notion. Qué pasa después de diciembre no
está escrito en ninguna fuente que se haya leído.

**Las metas comprometidas — la definición formal de éxito:**

| Frente | Meta comprometida | Cómo se mide |
|---|---|---|
| Entrevista | **No encontrada.** Ver el aviso de abajo. | — |
| Vacantes | **No encontrada.** | — |
| Comercial | **No encontrada.** | — |
| Incubación | **No encontrada.** | — |

**Fuente única y válida de estas metas:** {{DONDE_VIVEN}} — no se localizó.

> 🔴 **No hay cifra de meta comprometida en ninguna fuente leída, y eso se
> escribe en vez de inventarse.** Lo que sí hay son objetivos técnicos de
> desempeño (peso de la landing, Lighthouse, tiempo de carga) que **no son la
> meta del negocio**: dicen qué tan rápido carga, no si va bien. Mientras esta
> tabla siga vacía, el vault puede registrar actividad pero **no puede
> responder "¿voy bien?"**. Es una limitación real del sistema, no un pendiente
> administrativo.
>
> Búsqueda hecha: las 17 filas de la base de Notion y todo el bundle del sitio.
> **No encontré, buscando así** — no afirmo que no exista.

---

## 5. Cómo trabajar conmigo

- Directo y crítico: señalar errores y empujar.
- **Breve por default.** Conclusión adelante, razonamiento después, y máximo
  cinco hallazgos por entrega. *(Regla puesta el 2026-09-17 por señal explícita:
  "fue mucho texto".)*
- Detallado solo cuando el tema lo pida o cuando se pida.
- Español.

---

## 6. Semáforo de autonomía

**🟢 Verde — decidir y seguir, sin marcar**
Crear una nota, enlazar, nombrar archivos, extraer hechos con su cita, aplicar
formato.

**🟡 Amarillo — decidir, seguir, y dejar el razonamiento por escrito**
Dónde archivar algo que cabe en dos lados · cómo nombrar una entidad nueva ·
declarar una nota rancia · resumir una fuente ambigua.
El razonamiento va en la nota misma o en `meta/bitacora.md`.

**🔴 Rojo — detenerse y preguntar**
Contradicciones sobre hechos con consecuencia: dinero, fechas comprometidas,
compromisos formales · borrar o fusionar notas existentes · **datos personales
identificables, siempre**.

Y dos rojos propios de este vault:

- 🔴 **Nada que sea credencial se escribe aquí**, ni siquiera disfrazado de
  enlace. Un enlace de invitación que da entrada a un equipo **es** una
  credencial. Se nombra el contenedor y el enlace se queda fuera.
- 🔴 **Este vault publica cuerpos** (`publica: "contenido"`). El chequeo
  automático de fugas atrapa matrícula, CURP, RFC y correo — **y no atrapa
  nombres de personas ni teléfonos**, que es justo de lo que están hechos los
  compromisos ajenos. Verificado el 2026-09-17. Antes de escribir un nombre,
  preguntar.

### El semáforo se calibra con el uso

Cada 🔴 que resulte innecesario baja a 🟡. Cada 🟡 que haya que corregir sube a
🔴. Los cambios se registran con fecha en `meta/decisiones.md`.

---

## 7. Estructura

```
CREA/
├── CLAUDE.md          este mapa
├── cerebro.json       la configuración de la herramienta
├── inbox/             buzón crudo. Se vacía al compilar
├── fuentes/           una ficha por fuente irrecuperable
├── notas/             conocimiento compilado. Un tema = un archivo
├── proyectos/         los frentes, uno por archivo
├── personas/          una ficha por contraparte recurrente
└── meta/
    ├── bitacora.md    qué compilé, qué no, y cuándo
    └── decisiones.md  decisiones del sistema y su porqué
```

**El kit no vive aquí.** Este repo son las notas. La herramienta se instala
aparte (`git clone <el kit> ~/cerebro && ~/cerebro/instalar.sh`) y ninguno de
los dos conoce la ruta del otro.

---

## 8. Convenciones

**Un tema = un archivo.** Es la regla donde estos sistemas se ganan o se pierden.

**Nombres:** minúsculas, guiones, sin acentos. `mi-proyecto.md`, no `Mi Proyecto.md`.

**Frontmatter obligatorio en toda nota:**

```yaml
---
titulo: Nombre legible
tipo: proyecto          # proyecto | nota | persona | fuente | decision
proyecto: entrevista    # o `transversal` si toca varios
tags: [uno, dos]
estado: activo          # activo | pausado | cerrado — solo si tipo es proyecto
actualizado: 2026-09-17
fuentes:
  - "De dónde salió esto"
relaciones:
  extiende: []
  contradice: []
  depende_de: []
---
```

**Enlaces `[[así]]` en el cuerpo**, siempre que se mencione otra entidad.

**Toda afirmación con consecuencia lleva cita** a la fuente de donde salió.

**No enlaces a `meta/` desde una nota publicable.** `meta/` no se publica, y un
enlace de una nota publicada a una que no lo es es un error de fuga en
`cerebro verificar`.

**`fuentes/` no guarda binarios.** Los originales se quedan donde ya viven.

**Ficha solo cuando la ficha aporta algo que la liga no:** original no
recuperable, o —sin ser minuta— sostiene una cifra o decisión citada. Lo
consultable con un clic lleva línea de cita con su URL:

```markdown
- 2026-06-17 · Decisión sobre X, junta con Y · https://...
```

---

## 9. Anatomía de una nota de proyecto

Toda nota en `proyectos/` mantiene estos bloques vivos:

1. **Estado hoy** — una frase. Lo primero que se lee.
2. **La meta**, textual y con su número.
3. **Numeralias** — cifras vigentes contra la meta, con fecha y fuente de cada una.
4. **Hitos** — cumplidos y próximos, con fecha.
5. **Decisiones tomadas** — qué, cuándo, quién, **y qué se descartó y por qué**.
6. **Compromisos ajenos** — quién debe qué, desde cuándo, a quién bloquea.
7. **Riesgos y contradicciones abiertas.**
8. **Fuentes.**

> Diez juntas sobre un proyecto no producen diez notas. Producen **una** nota de
> proyecto actualizada, con diez fuentes citadas al pie.

---

## 10. El loop

1. **Capturar** — todo cae en `inbox/` sin decidir dónde va.
2. **Compilar** — leer lo nuevo, escribir o actualizar notas, enlazar, marcar
   contradicciones, **cruzar frentes**, vaciar el buzón, y escribir la bitácora.
3. **Usar** — responder desde las notas, siempre con cita. **Si algo no está,
   decir que no está.** Nunca rellenar con suposiciones.

---

## 11. De dónde sale el material

Seis contenedores, con su estado de acceso verificado el **2026-09-17**:

| Fuente | Qué es | Acceso |
|---|---|---|
| **Repositorio** — `TheIns07/entrevist-ia` | El código del producto. **Fuente primaria** | ✅ Público. Clon superficial: sin historial ni PRs |
| **Notion** — espacio `inscreup`, base *Incubadora de proyectos* | El tablero del sprint. 17 elementos | ⚠️ Parcial: solo por el sitio público. El conector está autenticado en otro workspace |
| **Sitio** — `entrevist-ia.netlify.app` | El producto desplegado | ⚠️ Parcial: es una SPA y las rutas internas dan 404; lo leído salió del bundle compilado |
| **Netlify** | Los despliegues | ⚠️ Parcial: `jobinderai` sí está en la cuenta conectada; **`entrevist-ia` no** — vive en otra |
| **Miro** | El tablero de armado de producto | 🔴 Sin acceso: el enlace exige unirse a otro equipo |
| **Figma** — *Entrenamiento Entrevistas IA* | Los diseños | 🔴 Sin acceso: la cuenta conectada no pertenece al plan del archivo |

**Trampas conocidas de estas fuentes** — verificadas, no heredadas:

- ⚠️ **Las propiedades de Notion no describen el avance.** Medido: `Priority`
  cubre 14 de 17 filas, y la columna de estado dice *Not started* en **17 de
  17** — 0% de señal, incluso en páginas que ya tienen trabajo escrito.
  Agrupar por ellas produce una nota falsa. Agrupa por contenido.
- ⚠️ **14 de las 17 páginas de Notion están vacías.** Solo tres tienen cuerpo.
  Un título no es una fuente: no cites una fila vacía como si dijera algo.
- 🔴 **El universo de fuentes no es el que te dieron.** Dos veces el 2026-09-17
  se escribió «no existe» sobre algo que sí existía, y las dos veces la causa
  fue la misma: **mirar solo los contenedores que estaban en la lista**. Antes de
  afirmar una ausencia, se barre la cuenta —repos, despliegues, proyectos— en vez
  de confiar en los enlaces recibidos. Vigilar una lista no sirve.
- 🔴 **El despliegue no es el código.** El 2026-09-17 el sitio iba atrasado
  respecto del repositorio y eso produjo una conclusión falsa. **El repositorio
  manda sobre el despliegue; los dos mandan sobre Notion.** Antes de afirmar que
  algo no existe, búscalo en el repo.
- ⚠️ **El repositorio no se documenta.** Su README es la plantilla por omisión
  de Vite. No lo cites como si describiera el proyecto.
- ⚠️ **El sitio no se puede leer como sitio.** WebFetch no ejecuta JS y las
  rutas internas devuelven 404. Lo que se lee es el bundle, que es **el código,
  no el comportamiento en vivo**: refleja lo que está escrito, no lo que
  responde el servidor ni lo que hay detrás del login.
- ⚠️ **Un resumen generado por IA no es el original.** Trae errores
  sistemáticos de nombres propios porque se genera sobre transcripción de
  audio. Pide el transcript antes de citar una cifra.
- ⚠️ **Una extracción vacía es una hipótesis sobre el extractor**, no un hecho
  sobre el documento.
- ⚠️ **Un sufijo de versión no significa que sea el archivo vigente.**
- ⚠️ **Figma tiene tope de 20 lecturas al mes** en el plan actual. No reintentes
  a ciegas mientras el permiso siga sin resolverse.

---

## 12. Lo que este vault no es

- **No es un gestor de tareas.** Aquí solo entran los compromisos *ajenos* que
  me bloquean.
- **No es un archivero.** Guardar sin compilar no cuenta. Una fuente sin nota
  destilada es trabajo pendiente, no conocimiento.
- **No es mi vida entera.** Solo CREA: lo personal y lo del Tec viven en el otro
  cerebro.
