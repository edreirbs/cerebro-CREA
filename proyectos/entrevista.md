---
titulo: Entrevista — el motor de entrevista y evaluación
tipo: proyecto
proyecto: entrevista
tags: [producto, entrevistia, piloto]
estado: activo
actualizado: 2026-09-17
fuentes:
  - "Notion · inscreup · base «Incubadora de proyectos», vista Priority board · leída 2026-09-17"
  - "Sitio desplegado · entrevist-ia.netlify.app · bundle compilado · leído 2026-09-17"
relaciones:
  extiende: []
  contradice: []
  depende_de: []
---

# Entrevista

> Nota piloto del vault: el paso 2 de `ARRANQUE.md` manda compilar **un solo
> frente, completo**, y éste es. Los otros tres frentes no se han compilado a
> propósito.

## 1. Estado hoy

Hay un producto desplegado y en uso mínimo, pero **lo que el sitio hace hoy no
es lo que el expediente dice que es**: el entrevistador es de texto, no de voz,
y el informe de evaluación está escrito a mano en el código.

## 2. La meta comprometida

**No la hay, o no se encontró.** Ninguna de las dos fuentes accesibles contiene
una meta de negocio con su número: ni usuarios, ni ingresos, ni conversión, ni
fecha de lanzamiento.

Lo que sí hay son **objetivos técnicos de desempeño**, que no son la meta:

- *"Landing inicial menor a aproximadamente 500 KB"*
- *"Lighthouse móvil superior a 90"*
- *"Tiempo de carga inicial inferior a 2 segundos en condiciones normales"*

— Notion, página *Stack Tecnologico*, sección Objetivos de performance, leída
2026-09-17.

**No encontré, buscando así:** las 17 filas de la base de Notion y el bundle
completo del sitio. No afirmo que la meta no exista — afirmo que no está en lo
que pude leer, y dos de las cuatro fuentes están cerradas.

## 3. Numeralias

| Cifra | Valor | Fecha | Fuente | Fidelidad |
|---|---|---|---|---|
| Elementos en el tablero del sprint | 17 | 2026-09-17 | Notion, vista Priority board | Original |
| De esos, con cuerpo escrito | 3 de 17 | 2026-09-17 | Notion | Original |
| Cobertura de la propiedad `Priority` | 14 de 17 filas | 2026-09-17 | Notion | Original |
| Filas marcadas *Not started* | 17 de 17 | 2026-09-17 | Notion, columna de estado | Original |
| Preguntas del banco de entrevista | 5, fijas (q1–q5) | 2026-09-17 | Bundle del sitio | Código, no comportamiento |
| Límite por respuesta | 500 caracteres | 2026-09-17 | Bundle del sitio | Código |
| Puntaje mostrado en resultados | 6.4, idéntico para todo usuario | 2026-09-17 | Bundle del sitio, objeto fijo | Código |
| Dimensiones de la rúbrica planeada | 7 | 2026-09-17 | Notion, tabla *Interview Evaluations* | Original |
| Rutas internas del sitio que responden | 0 de 8 | 2026-09-17 | Peticiones HTTP al dominio | Verificado dos veces |

> 🔴 **Ninguna de estas cifras ha salido del vault.** Antes de que alguna entre
> a un pitch o a un reporte, se verifica contra el original — las de adentro se
> corrigen, las presentadas ya no.

## 4. Hitos

- **jun 2026 – dic 2026** — ventana declarada del sprint de incubación CREA.
  Fuente: descripción interna de la base de Notion. *No visible en el tablero
  renderizado; solo en los metadatos de la base.*
- **2026-07-03** — edición más antigua registrada en el tablero.
- **2026-09-12** — se editan 10 de las 17 filas el mismo día.
- **2026-09-15** — última edición de *Pitch de venta: Elevator pitch*.
- **2026-09-17** — última edición de *Scrapper*, el elemento más reciente.
- **Próximos: no hay ninguno con fecha** en ninguna fuente leída. No hay
  roadmap, changelog ni fecha de lanzamiento.

## 5. Decisiones tomadas

Registradas con la cautela que merecen: **el tablero documenta elecciones
técnicas pero no dice quién las tomó ni cuándo**, así que van sin autor y sin
fecha, que es un hueco del expediente, no un dato.

- **Entrevista por voz** sobre WebRTC, Web Audio API y MediaDevices API.
  Fuente: Notion, *Stack Tecnologico*. **Descartado:** no consta.
- **Evaluación por rúbrica de 7 dimensiones** (overall, clarity, structure,
  evidence, relevance, communication, confidence). Fuente: Notion, *Base de
  datos*, tabla *Interview Evaluations*.
- **Control de costo por usuario** con tabla `Usage` dedicada. Fuente: Notion,
  *Base de datos*. Es la decisión que hace de este frente un frente: tiene
  presupuesto propio y está declarado.
- **Rerank con IA sobre un TOP 12 local para devolver un TOP 5.** Fuente:
  Notion, *Scrapper*. Pertenece al frente [[vacantes]], se anota aquí por el
  pipeline compartido.

**Hueco:** no hay una sola decisión en el expediente con la forma completa que
pide el método — qué, cuándo, quién, y qué se descartó y por qué. Esa cuarta
parte, la alternativa descartada, no aparece en ninguna fuente.

## 6. Compromisos ajenos

**Ninguno capturado**, y no porque no existan: la compilada del 2026-09-17 se
hizo con la regla de no escribir nombres de personas, y sin nombre un
compromiso no es accionable. Dos bloqueos sí están identificados y necesitan
que alguien les ponga nombre y rol:

| Qué hace falta | A quién bloquea | Desde |
|---|---|---|
| Acceso de lectura al archivo de Figma *Entrenamiento Entrevistas IA* | A toda compilada de diseño de este frente | 2026-09-17 |
| Entrada al equipo de Miro donde vive el tablero de producto | A toda compilada de producto | 2026-09-17 |

## 7. Riesgos y contradicciones abiertas

### Contradicciones — registradas, no resueltas

**C1 · La voz.** Notion describe un entrevistador hablado sobre WebRTC, Web
Audio API y MediaDevices API (*Stack Tecnologico*, 2026-09-12), y la portada
promete textualmente *"Respondes en voz alta a un entrevistador con IA"*. El
bundle desplegado tiene **cero** ocurrencias de `getUserMedia`,
`MediaRecorder`, `SpeechRecognition`, `speechSynthesis` y `AudioContext`; las
respuestas se escriben en un campo de texto de 500 caracteres.

**C2 · La evaluación.** Notion describe una rúbrica de 7 dimensiones
persistida en base de datos. El sitio muestra un objeto fijo escrito en el
código: puntaje 6.4 y desglose 8, 7, 8, 3, 6, **igual para todo usuario**.

**C3 · La infraestructura.** Notion nombra Cloudflare Workers y un esquema de
6 tablas (`Users`, `Candidate Profiles`, `Interview Sessions`,
`Interview Turns`, `Interview Evaluations`, `Usage`). El sitio corre sobre
Netlify Edge Functions y su cliente habla con 5 tablas de nombres distintos
(`profiles`, `interview_sessions`, `interview_questions`,
`interview_answers`, `interview_results`).

**C4 · Las vacantes.** El pipeline completo del *Scrapper* está documentado en
Notion. En el sitio desplegado no hay rastro de él. Ver [[vacantes]].

> 🟡 **Hipótesis que reconciliaría las cuatro, marcada como hipótesis y no como
> hecho:** Notion describe la arquitectura **objetivo** del sprint y el sitio
> es el **estado actual** del prototipo. Encaja con las cuatro, pero **ninguna
> fuente lo dice**. No se promedia, no se elige la más reciente: se pregunta.
>
> **La pregunta exacta para quien decide:** ¿el contenido de Notion es el plan
> de diciembre o la descripción de lo que ya existe? De la respuesta depende si
> C1–C4 son deuda de producto o errores del expediente.

### Riesgos

**R1 · La portada promete lo que el producto no hace.** Voz, y un testimonial
de *"contratada en 2 semanas"*, contra un producto que escribe y devuelve el
mismo 6.4 a todos. El daño no es técnico: es que una demo delante de la
contraparte de incubación o de un comprador B2B lo descubre en vivo. Toca
también [[comercial]].

**R2 · El sitio está roto para cualquier enlace directo.** Las 8 rutas internas
(`/login`, `/dashboard`, `/onboarding`, `/terms`, `/privacy`, …) devuelven 404:
falta la regla de reescritura de SPA. Quien reciba un enlace profundo, o quien
recargue la página, ve el 404 de Netlify. Es el defecto más barato de arreglar
de esta lista: una regla `/* /index.html 200`.

**R3 · Dos de las cuatro fuentes están cerradas.** Miro y Figma. Mientras sigan
así, **toda compilada de este frente es parcial por construcción**, y el diseño
—que es donde suele vivir la decisión de producto— no entra al vault.

**R4 · El expediente no registra alternativas descartadas.** Sin ellas, cada
decisión de arquitectura se va a volver a discutir. Es el bloque que más vale a
los seis meses y hoy está vacío.

## 8. Cobertura de esta compilada

- **Universo:** 4 contenedores declarados. **Leídos: 2.** Miro y Figma quedaron
  fuera por falta de permiso, no por criterio.
- **Notion:** 17 de 17 filas abiertas, pero **solo 3 tienen cuerpo**. Todo lo
  que se sabe de Comercial, Producto y Tracción viene **únicamente de títulos**.
- **Sin leer, y es material:** los dos diagramas embebidos desde Figma dentro de
  *Stack Tecnologico*; las secciones 6 a 12 de esa misma página, que no
  aparecen en el render público — el documento salta de «5. Base de datos» a
  «13. Registro» y no sé si están ocultas o nunca se escribieron; comentarios e
  historial de versiones de Notion.
- **Sitio:** nunca se vio renderizado ni autenticado. Todo salió del bundle
  compilado. **Nada de lo que hay detrás del login se compiló**, ni un solo
  dato real de la base.
- **Fidelidad:** todo lo de esta nota salió de originales —tablero y código—,
  **nada de resúmenes**. Pero «original» aquí significa *el código escrito*, no
  *el sistema corriendo*, y no es lo mismo.

## 9. Fuentes

- 2026-09-17 · Notion, base *Incubadora de proyectos*, vista *Priority board* · https://inscreup.notion.site/38ce78250e0880d39c33ec11ac0277c9
- 2026-09-17 · Sitio desplegado, leído del bundle compilado · https://entrevist-ia.netlify.app/
- 2026-09-17 · Figma, *Entrenamiento Entrevistas IA* — **sin acceso de lectura** · https://www.figma.com/design/ewxHYLjZkfq8ZBra53Qbe9/

Y una cuarta sin liga, a propósito: el tablero de **Miro** de armado de
producto. Su enlace de invitación no se guarda aquí porque da entrada a un
equipo — es credencial, y las credenciales no van en un archivo versionado.
