# Subdominios

> Estado: borrador. Agrupación de los eventos del [Event Storming](02-event-storming.md).

## Tipos de subdominio

- **Core**: lo que diferencia a Edooca. Aquí va el mejor diseño y el mayor esfuerzo.
- **Supporting**: necesario y propio de Edooca, pero no es la razón por la que la eligen.
- **Generic**: problema resuelto por otros; se compra, se usa una librería o un servicio.

## Propuesta

| Subdominio | Tipo | Qué cubre | Eventos |
|---|---|---|---|
| **Creación de contenido** | Core | Retos, pruebas, preguntas y sus tipos | 7, 8, 9, 11 |
| **Evaluación y nivel** | Core | Corregir intentos y determinar el nivel por asignatura | 16, 17, 21 |
| **Realización** | Supporting | Asignar contenido y que el estudiante haga intentos | 12–15, 18 |
| **Familia** | Supporting | Tutores, estudiantes, relación y visibilidad entre tutores | 1, 3–6 |
| **Puntos** | Supporting | Ganar y canjear puntos | 19, 20 |
| **Notas escolares** | Supporting | Registrar notas del colegio e importarlas | 22, 23 |
| **Generación con IA** | Generic | Llamar a un modelo generativo para producir contenido | 10 |
| **Identidad y acceso** | Generic | Registro, login, cuentas | 2 |

Fuera del Event Storming, pero probablemente necesarios más adelante: notificaciones y
pagos o suscripciones (Generic).

## Decisiones tomadas

- El **core** son dos subdominios: **Creación de contenido** y **Evaluación y nivel**.
  Lo que diferencia a Edooca es el ciclo "el tutor crea contenido para su estudiante →
  sabe de verdad qué nivel tiene". Ahí va el mayor esfuerzo de diseño.
- **Realización** se queda como supporting. Si la experiencia del estudiante llega a ser
  un diferenciador (p. ej. formato tipo juego), se revisa.
