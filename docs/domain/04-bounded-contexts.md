# Bounded contexts

> Estado: borrador. Basado en los [subdominios](03-subdomains.md).

Un bounded context es una frontera en la solución dentro de la cual cada término del
[glosario](glossary.md) tiene un único significado y un único modelo.

## Propuesta

| Contexto | Subdominio | Tipo | Responsabilidad |
|---|---|---|---|
| **Familia** | Familia | Supporting | Tutores, estudiantes, relación y visibilidad entre tutores |
| **Autoría** | Creación de contenido | Core | Crear y editar retos, pruebas y preguntas, a mano o con IA |
| **Realización** | Realización | Supporting | Asignar contenido y registrar los intentos y respuestas del estudiante |
| **Evaluación** | Evaluación y nivel | Core | Corregir intentos y determinar el nivel por asignatura |
| **Puntos** | Puntos | Supporting | Saldo de puntos: ganarlos y canjearlos |
| **Expediente escolar** | Notas escolares | Supporting | Notas del colegio, registradas o importadas |

Sistemas externos (Generic), siempre detrás de una interfaz propia:

- **Proveedor de identidad**: registro y login.
- **Proveedor de IA generativa**: lo usa Autoría para generar contenido.
- **Plataformas escolares** (p. ej. Educamos): las usa Expediente escolar para importar notas.

## El mismo término en distintos contextos

| Término | Familia | Autoría | Realización | Evaluación | Puntos |
|---|---|---|---|---|---|
| **Estudiante** | Perfil, relación con sus tutores | — | Quien hace intentos | Sus niveles por asignatura | Su saldo |
| **Reto / Prueba** | — | Contenido editable, con soluciones | Lo asignado: se muestra sin soluciones | Las soluciones y criterios para corregir | — |
| **Tutor** | Miembro con permisos y visibilidad | Autor del contenido | Quien asigna | Quien corrige respuestas abiertas | — |

## Cómo se comunican

Mediante **eventos de dominio**, sin compartir modelos. Por ejemplo:

1. Autoría publica un reto → Realización permite asignarlo.
2. Realización: *Intento completado* → Evaluación lo corrige.
3. Evaluación: *Intento corregido* → Puntos suma puntos.
4. Evaluación: *Nivel actualizado* → el tutor lo ve en su seguimiento.
5. Puntos: *Puntos canjeados* → Realización permite repetir la prueba.

El detalle de estas relaciones se define en el context map (paso 5).

## Decisiones tomadas

- **Al asignar, el contenido se congela.** Realización guarda una copia del reto o la
  prueba tal como estaba en el momento de asignarlo. Si el tutor lo edita después, las
  asignaciones existentes no cambian; los cambios solo afectan a las asignaciones nuevas.
  **Por qué**: los intentos de una misma asignación son comparables entre sí, y el
  estudiante no ve cambiar lo que está haciendo.

## Preguntas abiertas

- ¿La visibilidad entre tutores la decide Familia y la aplican los demás contextos?
