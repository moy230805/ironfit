# Iron Fit - Sistema de Gestión para Gimnasio

Proyecto de la materia **Arquitectura de Software** (Actividad Integradora).

**CETI** - Ingeniería en Sistemas Computacionales - Grupo 5B

## Equipo
- Noe Alejandro Valdez Valtierra (24310408)
- Moisés Josafat Madera Ramírez (24310018)

## Descripción
Sistema web para la gestión de un gimnasio pequeño ficticio llamado "Iron Fit". Permite administrar socios, pagos, clases y asistencia.

## Tecnologías
- HTML5
- CSS3
- JavaScript (vanilla)
- MySQL (script incluido en `/sql`)

> **Nota:** Como no tenemos un servidor backend en este proyecto, los datos se simulan con `localStorage` del navegador. El script SQL está incluido para referencia de la estructura de base de datos.

## Estructura del proyecto
```
iron-fit/
├── index.html          (login)
├── README.md
├── css/
│   └── styles.css      (estilos generales)
├── js/
│   ├── data.js         (datos y funciones de localStorage)
│   └── utils.js        (funciones auxiliares)
├── pages/
│   ├── dashboard.html  (panel principal)
│   ├── socios.html     (gestión de socios)
│   ├── pagos.html      (control de pagos)
│   ├── clases.html     (horarios y clases)
│   └── asistencia.html (registro de asistencia)
└── sql/
    └── iron_fit.sql    (script de base de datos)
```

## Módulos
1. **Login** - Autenticación de usuarios (admin, recepción, entrenador)
2. **Dashboard** - Métricas, últimos pagos, clases del día, alertas
3. **Socios** - Alta, baja, edición y búsqueda de miembros
4. **Pagos** - Registro de pagos con semáforo de estado (verde/amarillo/rojo)
5. **Clases** - Configuración de horarios con validación de traslape
6. **Asistencia** - Registro de asistencia por clase y fecha

## Cómo usar
1. Abrir `index.html` en un navegador
2. Iniciar sesión con:
   - **Admin:** admin@ironfit.com / admin123
   - **Recepción:** maria@ironfit.com / recep123

## Arquitectura
Se utiliza el patrón **MVC** (Modelo-Vista-Controlador):
- **Modelo:** `data.js` (funciones de acceso a datos)
- **Vista:** archivos HTML + CSS
- **Controlador:** scripts dentro de cada página HTML
