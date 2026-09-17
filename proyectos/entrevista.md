---
titulo: Entrevista — el motor de entrevista y evaluación
tipo: proyecto
proyecto: entrevista
tags: [producto, entrevistia, piloto]
estado: activo
actualizado: 2026-09-17
fuentes:
  - "Repositorio · github.com/TheIns07/entrevist-ia · commit e9724fe, 2026-09-16 · leído 2026-09-17"
  - "Notion · base «Incubadora de proyectos», vista Priority board · leída 2026-09-17"
  - "Sitio desplegado · entrevist-ia.netlify.app · bundle compilado · leído 2026-09-17"
relaciones:
  extiende: []
  contradice: []
  depende_de: []
---

# Entrevista

> Nota piloto del vault: el paso 2 de `ARRANQUE.md` manda compilar **un solo
> frente, completo**, y éste es. Los otros tres no se han compilado a propósito.

## 1. Estado hoy

El producto está **más avanzado en el repositorio que en lo desplegado**: la
entrevista por voz ya está escrita y no está en el aire, y el informe de
resultados sigue siendo un objeto de prueba escrito a mano.

## 2. La meta comprometida

**No la hay, o no se encontró.** Ninguna de las tres fuentes accesibles contiene
una meta de negocio con su número: ni usuarios, ni ingresos, ni conversión, ni
fecha de lanzamiento. El repositorio tampoco: su README es **la plantilla por
omisión de Vite**, sin una línea propia del proyecto.

Lo que sí hay son objetivos técnicos de desempeño —*"landing menor a 500 KB"*,
*"Lighthouse móvil superior a 90"*, *"carga inferior a 2 segundos"* (Notion,
*Stack Tecnologico*)— que dicen qué tan rápido carga, no si va bien.

**No encontré, buscando así:** 17 filas de Notion, el bundle del sitio y el
árbol completo del repositorio. No afirmo que la meta no exista.

## 3. Numeralias

| Cifra | Valor | Fecha | Fuente | Fidelidad |
|---|---|---|---|---|
| Último commit del repositorio | `e9724fe`, *Protected routes ix* | 2026-09-16 | Repo | Original |
| Páginas de la aplicación | 13 | 2026-09-17 | Repo, `src/pages/` | Original |
| Edge functions escritas | 2 — `analyze-resume`, `transcribe-audio` | 2026-09-17 | Repo, `supabase/functions/` | Original |
| Tablas que el código realmente usa | 4 — `profiles`, `interview_sessions`, `interview_answers`, `interview_results` | 2026-09-17 | Repo, llamadas `.from()` | Original |
| Tablas que Notion planea | 6 | 2026-09-17 | Notion, *Base de datos* | Original |
| Archivos de datos simulados | 3 — `mockResults`, `mockDashboard`, `mockInterview` | 2026-09-17 | Repo, `src/mocks/` | Original |
| Puntaje mostrado en resultados | 6.4, escrito a mano | 2026-09-17 | Repo, `src/mocks/mockResults.ts:23` | Original |
| Elementos en el tablero del sprint | 17, de los cuales **3 con cuerpo** | 2026-09-17 | Notion | Original |
| Cobertura de la propiedad `Priority` | 14 de 17 filas | 2026-09-17 | Notion | Original |
| Filas marcadas *Not started* | 17 de 17 | 2026-09-17 | Notion | Original |
| Rutas internas del sitio que responden | 0 de 8 | 2026-09-17 | Peticiones HTTP | Verificado |

> 🔴 **Ninguna de estas cifras ha salido del vault.** Antes de que alguna entre
> a un pitch se verifica contra el original.

## 4. Hitos

- **jun 2026 – dic 2026** — ventana del sprint de incubación CREA. Fuente:
  descripción interna de la base de Notion, no visible en el tablero renderizado.
- **2026-09-12** — se editan 10 de las 17 filas de Notion el mismo día.
- **2026-09-16** — último commit del repositorio.
- **2026-09-17** — última edición de *Scrapper* en Notion.
- **Próximos: ninguno con fecha** en ninguna fuente. No hay roadmap ni changelog.

## 5. Decisiones tomadas

El expediente documenta elecciones técnicas pero **no dice quién las tomó ni
cuándo**, así que van sin autor: es un hueco, no un dato.

- **Entrevista por voz**, y ya está construida: `src/components/voice/VoiceInputButton.tsx`,
  `src/services/ai/transcription.service.ts` y la edge function `transcribe-audio`.
  Usa `getUserMedia`, `MediaRecorder` y `AudioContext`. **Descartado:** no consta.
- **Supabase Edge Functions** como servidor, no Cloudflare Workers. El repo no
  tiene una sola mención de Cloudflare. Corrige lo que dice Notion.
- **Análisis de CV con IA** en la edge function `analyze-resume`, con un motor
  de PDF propio y extenso (`src/lib/pdf-engine/`, 11 submódulos).
- **Rutas protegidas** con `src/routes/ProtectedRoute.tsx`, que es el trabajo
  del último commit.
- **Evaluación por rúbrica de 7 dimensiones**: sigue siendo **solo plan de
  Notion**. Lo que corre es un mock.

**Hueco:** ninguna decisión del expediente trae su alternativa descartada. Es el
bloque que más vale a los seis meses y está vacío.

## 6. Compromisos ajenos

**Ninguno con nombre**, por la regla de datos personales. Pero **las fuentes de
este proyecto son todas ajenas**, así que cada bloqueo de acceso *es* un
compromiso ajeno y envejece como tal:

| Qué hace falta | Quién puede darlo | A quién bloquea | Abierto desde |
|---|---|---|---|
| Lectura del archivo de Figma | quien es dueño del archivo o administra su plan | toda compilada de diseño | 2026-09-17 |
| Entrada al equipo de Miro | quien administra ese equipo | toda compilada de producto | 2026-09-17 |
| Acceso al Netlify de EntrevistIA | quien despliega el sitio | verificar qué está en el aire contra el repo | 2026-09-17 |

**Y uno que sí es tuyo y se parece a los otros:** el conector de Notion está
autenticado en un workspace distinto de `inscreup`, así que el tablero se lee
solo por su sitio público. Eso limita la compilada a lo publicado — sin
comentarios, sin historial, sin propiedades ocultas.

## 7. Riesgos y contradicciones abiertas

**El repositorio resolvió una de las cuatro contradicciones y confirmó las
otras tres.** La pregunta *"¿Notion es el plan o la realidad?"* ya tiene
respuesta, y es **mixta y medible**: una parte ya se construyó, dos siguen
siendo plan, y una es error de Notion.

### C1 · La voz — **CERRADA el 2026-09-17. Notion tenía razón.**
La entrevista por voz **sí está implementada** en el repositorio. El error era
mío: lo concluí del bundle desplegado, y **el despliegue está atrasado respecto
del repositorio**. El detalle y la regla que produjo están en
`meta/decisiones.md`.
**Lo que queda no es contradicción sino deuda:** está escrita y no está en el
aire.

### C2 · La evaluación — **CONFIRMADA, y es peor de lo que parecía.**
No es que el bundle viejo tuviera un valor fijo: `src/pages/ResultsPage.tsx`
importa de `src/mocks/mockResults.ts`, donde `score: 6.4` está escrito a mano.
El dashboard hace lo mismo (`mockDashboard.ts`, dos veces). **La rúbrica de 7
dimensiones que Notion documenta no existe en el código.** Todo usuario que
termine una entrevista ve el mismo resultado.

### C3 · La infraestructura — **CONFIRMADA, y el error es de Notion.**
Notion nombra Cloudflare Workers y un esquema de 6 tablas. El código no
menciona Cloudflare ni una vez y usa **4 tablas**: `profiles`,
`interview_sessions`, `interview_answers`, `interview_results`. El expediente
de Notion describe una arquitectura que no es la que se construyó.

### C4 · Las vacantes — **CONFIRMADA dentro del alcance de CREA: es plan.**
Cero rastro en el repositorio de EntrevistIA: ni proveedores de empleo, ni
*scrapping*, ni *matching*. El pipeline existe solo como documento de Notion.

**Lo que se rechazó, y por qué se anota:** el barrido de la cuenta de Netlify
del 2026-09-17 encontró un producto desplegado que hace algo parecido. **No
pertenece a CREA** y quedó fuera por decisión del 2026-09-17 — la primera vez
que este vault ejerce su lista blanca. Se nombra sin enlace ni detalle, como
manda la regla: *lo que no encaja se reporta y se deja donde está*. Ver
[[vacantes]] cuando ese frente se compile.

### Riesgos

**R1 · El informe de resultados es de mentira y está en producción.** Es el
riesgo más alto de la lista. Cualquiera que pruebe el producto dos veces con
respuestas distintas ve el mismo 6.4. En una demo ante la contraparte de
incubación o un comprador, se descubre solo. Toca también [[comercial]].

**R2 · El sitio está roto para cualquier enlace directo.** 8 de 8 rutas internas
dan 404. **Causa localizada en el repositorio:** no existen `netlify.toml` ni
`public/_redirects`, así que falta la regla de reescritura de SPA. Es el arreglo
más barato de toda la nota: un archivo de dos líneas.

**R3 · El despliegue está atrasado respecto del repositorio.** La voz es la
prueba. Mientras eso siga así, **lo que se demuestra no es lo que se construyó**,
y quien juzgue el avance por el sitio va a subestimarlo.

**R4 · El repositorio no se documenta a sí mismo.** Su README es la plantilla
por omisión de Vite. Toda la documentación del proyecto vive en Notion, que ya
sabemos que describe otra arquitectura.

**R5 · Dos de las cinco fuentes siguen cerradas** — Miro y Figma. El diseño, que
es donde suele vivir la decisión de producto, no entra al vault.

## 8. Cobertura de esta compilada

- **Universo: 5 contenedores. Leídos: 3.** Miro y Figma quedaron fuera por falta
  de permiso, no por criterio.
- **Repositorio:** clon superficial (`--depth 1`), así que **solo se vio el
  último commit**: no hay historial, ni ramas, ni PRs, ni issues. No se leyó el
  contenido de los archivos fuente salvo por búsquedas dirigidas; no se corrió
  ni se compiló nada.
- **Notion:** 17 de 17 filas abiertas, **solo 3 con cuerpo**. Comercial,
  Producto y Tracción se conocen únicamente por títulos.
- **Sitio:** nunca se vio renderizado ni autenticado. Y ahora sabemos que
  además **estaba desactualizado**, así que las conclusiones que salieron de ahí
  valen menos que las del repositorio.
- **Fidelidad:** todo de originales, nada de resúmenes. Pero «original» tiene
  tres capas distintas —repositorio, despliegue y tablero— y **no dicen lo
  mismo**. El repositorio manda sobre el despliegue; ambos mandan sobre Notion.

## 9. Fuentes

- 2026-09-17 · Repositorio, commit `e9724fe` del 2026-09-16 · https://github.com/TheIns07/entrevist-ia
- 2026-09-17 · Notion, base *Incubadora de proyectos* · https://inscreup.notion.site/38ce78250e0880d39c33ec11ac0277c9
- 2026-09-17 · Sitio desplegado, leído del bundle · https://entrevist-ia.netlify.app/
- 2026-09-17 · Figma, *Entrenamiento Entrevistas IA* — **sin acceso** · https://www.figma.com/design/ewxHYLjZkfq8ZBra53Qbe9/

Y una quinta sin liga a propósito: el tablero de **Miro**. Su enlace de
invitación da entrada a un equipo — es credencial, y no va versionado.
