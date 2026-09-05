# 🗒️ Registro de Trabajo en Clase - Taller 3

## 📆 Fecha de la sesión
04/09/2026

## 👥 Integrantes presentes
- Esteban Díaz
- Juliana Moreno

## 🧠 Actividades realizadas en clase

Durante la sesión se trabajó la **Parte 1: Trabajo en Clase** del Taller 3 de Arquitectura Actual del Sistema con el Modelo C4.

Se trabajó en el caso de **RedExpress**. Se siguió la metodología indicada para construir las dos primeras vistas del modelo C4:

- **C1 - Vista de Contexto:** se identificaron los actores que interactúan directamente con la plataforma, el sistema en alcance y los sistemas externos.
- **C2 - Vista de Contenedores:** se descompuso la Plataforma RedExpress en sus principales aplicaciones, servicios e infraestructura de soporte.
- Se identificaron y etiquetaron las principales relaciones e interacciones entre los elementos.
- El modelado se realizó directamente en **draw.io**.

### Decisiones de modelado

En la vista C1 se mantuvo la **Plataforma RedExpress como una única caja**, sin mostrar sus componentes internos. Se incluyeron los actores Usuario Final, Mensajero y Operador Logístico, además de la API de Notificaciones y el Proveedor de Geolocalización como sistemas externos.

En la vista C2 se descompuso la plataforma en App Móvil, Portal Web Operadores, Módulo de Gestión de Paquetes, Motor de Rutas, Seguimiento GPS y Sistema de Alertas. Como infraestructura se incluyeron el Balanceador de Carga y la Base de Datos Distribuida.

Las relaciones fueron etiquetadas para indicar qué información se intercambia en C1 y los protocolos o mecanismos de comunicación utilizados en C2.

## 🧩 Boceto inicial del modelo

**No hubo boceto inicial.** Realizamos directamente los diagramas en draw.io.

## 🔁 Tareas definidas para complementar el taller

| Tarea asignada | Responsable | Fecha estimada |
|---|---|---|
| Modelado en draw.io | Esteban Díaz | 04/09/2026 |
| Redacción del informe | Juliana Moreno | 04/09/2026 |
| Investigación y referencias | Juliana Moreno | 04/09/2026 |

## 📝 Observaciones

La actividad permitió establecer la diferencia entre los niveles C1 y C2 del modelo C4 y organizar la arquitectura actual de RedExpress de acuerdo con el nivel de abstracción correspondiente.

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del Taller 3 en el curso AREM - Universidad de La Sabana._
