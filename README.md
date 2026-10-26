# TaskStudy

Aplicación móvil nativa para Android orientada a la gestión de tareas académicas de estudiantes universitarios.

**Universidad de Cundinamarca · Ingeniería de Software · 2026**
**Asignatura:** Desarrollo de Aplicaciones Nativas para Dispositivos Móviles (Proyecto Integrador Internacionalizado, POO + Aplicaciones Nativas)
**Docente:** Iván Darío Callejas Sandoval

## Integrantes

| Integrante | Rol en el proyecto |
|---|---|
| Brayan Alexander Castro Esquivel | Configuración base y pantalla de inicio de sesión |
| Sara Valeria Galindo Gómez | Diseño de interfaz, pantalla de inicio y actividades |
| Brandon David Mogollón Monsalve | Formulario de nueva tarea y componentes reutilizables |

## Descripción del problema

Los estudiantes universitarios reparten su atención entre varias asignaturas, entregas y trabajos prácticos. Sin una herramienta centralizada, la información se dispersa entre agendas, mensajes y recordatorios informales, lo que causa olvido de fechas de entrega y dificultad para priorizar.

TaskStudy centraliza esa información: el usuario registra tareas por materia, adjunta archivos, define la fecha de entrega y consulta lo pendiente del día.

## Funcionalidades previstas (MVP)

- Registro e inicio de sesión (solo interfaz en esta etapa).
- Listado de tareas pendientes del día en la pantalla de inicio.
- Creación de tareas con materia, archivos adjuntos y fecha de entrega.
- Marcar una tarea como realizada.
- Consulta de actividades filtradas por **Hoy**, **Esta semana** y **Próximas**.
- Barra de navegación inferior común a las pantallas principales.

## Estado actual del proyecto

- Diseño de alta fidelidad (mockups) de las cuatro pantallas principales.
- Proyecto creado en Android Studio con las vistas maquetadas en XML.
- Estructura de paquetes `adapter`, `data` y `model`.
- Pendiente: lógica de negocio (persistencia, autenticación real, manejo de adjuntos) y navegación funcional entre actividades.

## Aportes de cada integrante

### Brayan Alexander Castro Esquivel
- Creó el proyecto **TaskStudy** en Android Studio y organizó la estructura de paquetes (`adapter`, `data`, `model`).
- Maquetó la pantalla de inicio de sesión y registro (`activity_sign_in.xml`) con el campo `etEmail` y los botones `btnIniciarSesion`, `btnGoogle` y `btnApple`.
- Extrajo la barra de navegación inferior a un layout independiente (`layout_bottom_nav.xml`) e incluyó mediante `<include>` en las pantallas.

### Sara Valeria Galindo Gómez
- Elaboró el diseño preliminar de alta fidelidad de las pantallas (Sign In, Home, New Task y Activities).
- Maquetó la pantalla de inicio (`activity_home.xml`) con el `RecyclerView` `rvTasks` y el ítem reutilizable `item_task.xml`.
- Añadió la pantalla de actividades (`activity_activities.xml`) con los filtros por chips (`chipHoy`, `chipSemana`, `chipProximas`) y el `RecyclerView` `rvActivities`.

### Brandon David Mogollón Monsalve
- Maquetó el formulario de nueva tarea (`activity_new_task.xml`) dentro de un `ScrollView`, con `etSubjectName`, `attachmentContainer` y `dateContainer`.
- Asignó identificadores descriptivos a los campos del formulario (`etSubjectName`, `ivAttach`, `tvAttach`) para facilitar su vinculación con el modelo de datos.
- Revisó la coherencia entre los requerimientos (RF01–RF05, RNF01–RNF03) y las vistas construidas.

## Estructura del proyecto

```
app/
└── src/main/
    ├── java/.../
    │   ├── adapter/
    │   ├── data/
    │   └── model/
    └── res/layout/
        ├── activity_sign_in.xml
        ├── activity_home.xml
        ├── activity_activities.xml
        ├── activity_new_task.xml
        ├── item_task.xml
        └── layout_bottom_nav.xml
```

## Tecnologías

- Android Studio
- Java / Kotlin (Android nativo)
- Layouts XML: `ConstraintLayout`, `LinearLayout`, `ScrollView`, `RecyclerView`

## Próximos pasos

- Implementar la navegación funcional entre las actividades ya maquetadas.
- Conectar las vistas con un modelo de datos inicial (adaptador con datos de prueba).
- Incorporar almacenamiento local y, más adelante, autenticación real.
- Agregar retroalimentación visual al marcar una tarea como realizada.

## Documentación

El informe de avance completo (R1-A1-S3) se encuentra en la carpeta `docs/`.
