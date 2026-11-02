# Visión de Edooca

> Estado: v1

## En una frase

Edooca es una plataforma familiar para que los padres acompañen la educación de sus
hijos: crean contenido y pequeños exámenes de distintas asignaturas, sus hijos los
realizan con su propia cuenta, y los padres siguen tanto el progreso dentro de
Edooca como las notas reales del colegio.

## Referencia

Un "Smartick orientado a padres": en Smartick el contenido lo decide la plataforma y
el alumno está en el centro; en Edooca el protagonista es el padre, que crea, asigna
y supervisa el aprendizaje de su hijo.

## Usuarios

- **Padre/madre (tutor)**: usuario principal. Crea contenido (a mano o con IA
  generativa), lo asigna a sus hijos y hace seguimiento de su evolución.
- **Hijo (alumno)**: tiene su propia cuenta y realiza los ejercicios y exámenes que
  le asigna su padre.

Es un producto **solo para la familia**: no intervienen profesores ni colegios como
usuarios.

## Problema que resuelve

Padres que necesitan recursos educativos rápidos para sus hijos y quieren algo más que
pedírselos a ChatGPT: contenido organizado por asignaturas, que el hijo pueda hacer
por su cuenta, y la posibilidad de hacer seguimiento y control de cómo avanza.

## Qué la hace especial

- **El padre crea el contenido**, adaptado a su hijo: definiéndolo a mano, generándolo
  con IA o combinando ambos.
- **Ciclo completo**: crear → asignar → el hijo lo realiza → el padre ve el resultado.
- **Dos visiones del progreso** del hijo, una junto a la otra:
  - **Progreso en Edooca**: resultados de los ejercicios y exámenes hechos en la plataforma.
  - **Notas escolares**: las calificaciones reales del colegio, introducidas por el
    padre o, en el futuro, importadas de plataformas escolares (p. ej. Educamos).

## Qué NO es Edooca

- No es un colegio online.
- No es un profesor particular.
- No es una herramienta para centros educativos ni profesores.

## Primeras pistas para el modelo

Notas para los pasos siguientes; no son decisiones todavía.

- "Nota" tiene **dos significados** distintos (progreso en Edooca vs. calificación del
  colegio). Conviene darles nombres diferentes en el lenguaje ubicuo.
- La integración con plataformas escolares es un sistema externo cuyo modelo no
  controlamos: candidata a una capa anticorrupción.
- La IA generativa es un medio para crear contenido, no el negocio en sí: probablemente
  un subdominio de apoyo o genérico, detrás de una interfaz propia.
