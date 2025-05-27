# Trabajo practico album de figuritas

# Simulación para completar el álbum de figuritas del Mundial

Dado un álbum con \( n \) figuritas diferentes, que se distribuyen aleatoriamente en cantidades iguales, se desea estimar cuántas figuritas (o paquetes) hay que comprar para completarlo.

---

## Datos

- Total de figuritas en el álbum: \( n \) (por ejemplo, \( n=640 \))
- Las figuritas se distribuyen aleatoriamente con igual probabilidad.
- Cada paquete contiene \( k \) figuritas (por ejemplo, \( k=5 \)) y pueden repetirse dentro del mismo paquete.

---

## Simulación de compra individual

Se modela la compra de figuritas individuales con el siguiente proceso:

1. Se elige una figurita aleatoria \( X_i \in \{1, \ldots, n\} \) con probabilidad uniforme.
2. Se repite la compra hasta haber obtenido todas las figuritas del álbum.

La cantidad total de figuritas compradas para completar el álbum es la variable aleatoria \( T \).

---

## Simulación de compra por paquetes

Cuando las figuritas se compran en paquetes de tamaño \( k \):

- Cada paquete es un vector aleatorio de \( k \) figuritas elegidas con reemplazo, \( P_j = (X_{j1}, \ldots, X_{jk}) \).
- Se acumulan figuritas paquete a paquete hasta completar el álbum.

La cantidad de paquetes comprados es la variable aleatoria \( M \).

---

## Objetivos de la simulación

- Estimar \( \mathbb{E}[T] \): la cantidad promedio de figuritas individuales necesarias para completar el álbum.
- Calcular \( \mathbb{P}(T \leq t) \): la probabilidad de completar el álbum con a lo sumo \( t \) figuritas.
- Determinar el valor \( t_{90} \) tal que \( \mathbb{P}(T \leq t_{90}) = 0.9 \) (es decir, completar el álbum con un 90% de probabilidad).
- Análogamente, estimar estos valores para la compra por paquetes.

---

## Herramientas implementadas en R

- Función para simular la compra individual hasta completar el álbum.
- Función para simular la compra por paquetes.
- Repeticiones múltiples para obtener estimaciones estadísticas.

---

Así, la simulación permite responder preguntas del tipo:

¿Cuántas figuritas hay que comprar, en promedio, para completar el álbum?

¿Cuál es la probabilidad de completarlo comprando a lo sumo

\[
P(T \leq t)
\]

figuritas?

¿Cuántas figuritas hay que comprar para tener un 90% de certeza de completarlo?


---

Esto es útil para comprender el fenómeno clásico del **problema del coleccionista de cupones** aplicado a los álbumes del Mundial.
