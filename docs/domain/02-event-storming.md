# Event Storming

> Estado: borrador. Eventos de dominio en pasado y en orden aproximado.
> Términos según el [glosario](glossary.md).

## Familia

1. Familia creada
2. Tutor registrado
3. Tutor añadido a la familia
4. Estudiante añadido a la familia
5. Cuenta del estudiante activada
6. Visibilidad entre tutores configurada

## Creación de contenido

7. Reto creado
8. Prueba creada
9. Pregunta añadida
10. Contenido generado con IA
11. Contenido generado revisado por el tutor

## Asignación y realización

12. Reto asignado al estudiante
13. Prueba asignada al estudiante
14. Intento iniciado
15. Intento completado
16. Respuesta corregida automáticamente
17. Respuesta abierta corregida por el tutor
18. Repetición de prueba solicitada
19. Puntos canjeados para repetir prueba

## Seguimiento

20. Puntos obtenidos
21. Nivel actualizado
22. Nota escolar registrada por el tutor
23. Notas escolares importadas desde la plataforma del colegio

## Decisiones tomadas

- Los perfiles se agrupan en una **Familia**, con dos roles: **Tutor** y **Estudiante**.
  La **relación** (padre, tío, hermano…) es una etiqueta y no afecta a los permisos.
- Un estudiante pertenece a **una sola familia**.
- Una familia puede tener **varios tutores**, y todos pueden crear contenido y añadir información.
- Entre tutores hay **visibilidad configurable**: un tutor puede ver o no ver lo que ha
  definido otro (p. ej. padres separados).
- "Ejercicio" y "examen" se llaman **Reto** (practicar) y **Prueba** (medir).
- La forma de una pregunta depende de su **tipo**, no de la asignatura.
- Se distingue el contenido (Reto/Prueba) de su realización (**Intento**).
- **Todo lo que hace el estudiante cuenta**: retos y pruebas suman puntos, y hacer más suma más.
- Una prueba **se puede repetir**, pagando un coste en puntos (por definir).
- **Puntos y Nivel son conceptos distintos** (ver abajo).

## Preguntas abiertas

- ¿Los retos influyen algo en el nivel, o solo las pruebas?
- ¿Los puntos son globales o por asignatura?
- ¿Qué se configura exactamente en la visibilidad: perfil del estudiante, contenido, resultados…?
- ¿Algún tutor tiene más permisos que otro (p. ej. quien gestiona la familia)?
- ¿El nivel es por asignatura, por tema, por curso? *(se revisa más adelante)*
- ¿Cuánto cuesta repetir una prueba y de qué depende? *(por definir)*
- ¿Con qué tipos de pregunta empezamos? *(se revisa más adelante)*

## Decisión: Puntos y Nivel por separado

Bajo la palabra "nivel" había dos ideas distintas:

| | **Puntos** | **Nivel** |
|---|---|---|
| Qué mide | Esfuerzo, constancia | Competencia, lo que sabe |
| Cómo se consigue | Haciendo cualquier reto o prueba; más actividad, más puntos | Sobre todo con pruebas |
| ¿Se gasta? | Sí (p. ej. repetir una prueba) | No |

**Por qué**: si fueran un solo número, un estudiante que practica mucho pero mal
tendría más nivel que uno que hace poco y perfecto, y canjear puntos para repetir
una prueba haría bajar lo que sabe. Separarlos mantiene limpia la medición de la
competencia y deja espacio para gamificación (recompensas, rachas…) sobre los puntos.
