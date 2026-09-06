# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

**Taller 3 - Arquitectura Actual del Sistema con el Modelo C4**

**Fecha:** 04/09/2026

## 👥 Integrantes del equipo

- Esteban Díaz
- Juliana Moreno

## 🧠 Descripción general del trabajo

El objetivo de la Parte 1 del taller fue representar la arquitectura actual del sistema de **RedExpress** utilizando las vistas C1 (Contexto) y C2 (Contenedores) del modelo C4.

RedExpress es una empresa nacional de logística y envíos que ofrece servicios de rastreo de paquetes y gestión de operaciones logísticas. Para representar su arquitectura se identificaron los principales actores que interactúan con el sistema, los sistemas externos y los componentes internos que permiten prestar sus servicios.

El trabajo se realizó directamente en **draw.io**. No se elaboró un boceto inicial previo.

## 🔧 Proceso de desarrollo

Primero se identificaron los actores de la vista de contexto: **Usuario Final, Mensajero y Operador Logístico**. Posteriormente se estableció la **Plataforma RedExpress** como sistema en alcance y se identificaron como sistemas externos la **API de Notificaciones** y el **Proveedor de Geolocalización**.

Para las relaciones del C1 se utilizaron etiquetas que describen las acciones o información intercambiada. El Usuario Final rastrea envíos y agenda recogidas; el Mensajero actualiza el estado de las entregas; y el Operador Logístico gestiona rutas y despachos. La plataforma utiliza la API de Notificaciones para enviar alertas de estado y el Proveedor de Geolocalización para consultar coordenadas y apoyar el cálculo de rutas.

Después se realizó el C2 mediante la descomposición de la Plataforma RedExpress. Se identificaron la **App Móvil**, el **Portal Web Operadores**, el **Módulo de Gestión de Paquetes**, el **Motor de Rutas**, el **Seguimiento GPS** y el **Sistema de Alertas**. También se representaron el **Balanceador de Carga** y la **Base de Datos Distribuida** como infraestructura de soporte.

Finalmente, se etiquetaron las relaciones del C2 con los mecanismos de comunicación correspondientes, entre ellos HTTPS/JSON, HTTPS, SQL, REST y Push/WebSocket.

## 🧩 Análisis del modelo propuesto

### Vista de Contexto (C1)

El C1 representa la Plataforma RedExpress como una sola unidad, permitiendo observar su relación con el entorno sin entrar todavía en su estructura interna. Los actores identificados representan los principales roles humanos que utilizan el sistema, mientras que la API de Notificaciones y el Proveedor de Geolocalización representan servicios externos con los que la plataforma se integra.

Esta separación permite mantener el nivel de abstracción del C1 y evitar incluir componentes internos que corresponden al nivel C2.

### Vista de Contenedores (C2)

El C2 amplía la Plataforma RedExpress y muestra los principales contenedores y elementos de infraestructura que la componen. Cada contenedor tiene una responsabilidad diferenciada.

La App Móvil permite la interacción de usuarios finales y mensajeros. El Portal Web permite al operador logístico gestionar las operaciones. El Módulo de Gestión de Paquetes centraliza la gestión de paquetes y coordina otros servicios. El Motor de Rutas permite solicitar rutas óptimas utilizando el proveedor de geolocalización. El Seguimiento GPS gestiona la ubicación en tiempo real y el Sistema de Alertas permite generar notificaciones.

El Balanceador de Carga distribuye las solicitudes hacia los servicios internos y la Base de Datos Distribuida permite persistir la información necesaria para la operación.

### Supuestos

Para el modelo se asumió que la API de Notificaciones y el Proveedor de Geolocalización son servicios externos a la Plataforma RedExpress. También se asumió que los actores interactúan con la plataforma mediante las aplicaciones correspondientes y que los contenedores internos se comunican mediante los protocolos indicados en la guía.

## 📈 Diagrama final entregado

El diagrama final fue elaborado en **draw.io** e incluye las vistas:

- **C1 - Vista de Contexto**
- **C2 - Vista de Contenedores**



## 📋 Tabla de actores, entidades o componentes

| Nombre del elemento | Tipo | Descripción | Responsable |
|---|---|---|---|
| Cliente | Actor | Solicita arreglos florales personalizados y consulta el estado de su pedido | Cliente |
| Propietario | Actor | Elabora los arreglos, gestiona el catálogo, precios y compras de materia prima | Equipo Oasis |
| Encargada de Atención | Actor | Revisa el panel de solicitudes pendientes y gestiona el contacto con los clientes | Equipo Oasis |
| Sistema Oasis | Sistema en alcance | Plataforma de gestión de clientes y pedidos a construir para el negocio | Equipo Oasis |
| WhatsApp Business API | Sistema externo | Envío automático de notificaciones de cambio de estado del pedido (Fase 3) | Proveedor externo (Meta) |
| App Web Oasis | Contenedor | Aplicación web ligera de acceso vía navegador, sin instalación | Equipo Oasis |
| API REST Oasis | Contenedor | Gestiona solicitudes, cotizaciones, pedidos, estados y notificaciones | Equipo Oasis |
| Base de Datos Oasis | Infraestructura | Almacenamiento SQL relacional de las 8 entidades del negocio | Equipo Oasis |

## 🔍 Investigación complementaria

### Tema investigado:

**Modelo C4 para la documentación de arquitectura de software: vistas de Contexto y Contenedores.**

### Resumen:

El modelo C4 permite representar la arquitectura de software mediante diferentes niveles de abstracción. La vista de contexto corresponde al nivel 1 y muestra el sistema en alcance junto con las personas y sistemas externos que interactúan con él. La vista de contenedores corresponde al nivel 2 y permite ampliar el sistema para mostrar las aplicaciones, servicios y almacenes de datos que lo componen. Esta separación ayuda a comunicar la arquitectura a diferentes tipos de audiencia y evita mezclar niveles de detalle.

Para este taller, la aplicación del modelo C4 permitió representar RedExpress primero desde una perspectiva general y posteriormente desde una perspectiva técnica. En C1 se priorizó la identificación de actores, sistemas externos y relaciones; en C2 se incorporaron los contenedores, la infraestructura y los mecanismos de comunicación. Esta forma de representación coincide con la estructura definida en la guía del taller y facilita validar que cada elemento tenga una responsabilidad y un nivel de abstracción adecuado.



## 📚 Referencias

Las referencias utilizadas y la información de investigación complementaria se encuentran registradas en `referencias.md`.

---

_Este documento hace parte de la entrega del Taller 3 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
