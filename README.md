Ecosistema de Trazabilidad Ganadera RFID

Este repositorio centraliza el desarrollo del sistema integral de gestión y trazabilidad individual de ganado mediante tecnología RFID (134.2 kHz). El ecosistema está diseñado para operar en entornos rurales con conectividad limitada, priorizando la portabilidad y la eficiencia operativa en la manga.
Estructura del Proyecto


## Estructura del Proyecto

El repositorio utiliza una arquitectura de "Monorepo" para agrupar los dos subsistemas principales, permitiendo una gestión unificada del ciclo de vida del software:

```text
Gestion-Ganadera-RFID/
├── README.md                   # Documentación principal del ecosistema
├── .gitignore                  # Exclusiones de Git para IntelliJ y Android Studio
│
├── Modulo-Movil-Android/       # Proyecto para el bastón RFID (Abrir en Android Studio)
│   ├── app/                    # Código fuente nativo en Java
│   ├── build.gradle            # Configuración de dependencias de Android
│   └── ...                     # Recursos y manifiesto de la aplicación
│
└── Modulo-Escritorio-PC/       # Proyecto de administración (Abrir en IntelliJ IDEA)
    ├── src/                    # Lógica de negocio y controladores (Java)
    ├── resources/              # Interfaces gráficas (FXML) y estilos (CSS)
    ├── pom.xml                 # Configuración de Maven / Dependencias JavaFX
    └── base_datos/             # Directorio para el archivo maestro de SQLite

Descripción de los Subsistemas
1. Módulo Móvil (Bastón RFID)

    Entorno de Desarrollo: Android Studio.

    Tecnologías: Java Nativo (SDK 21/22), SQLite.

    Propósito: Captura ágil de datos en campo, ejecución de tareas con formularios dinámicos y alertas sanitarias en tiempo real sin necesidad de conexión a internet.

2. Módulo de Administración (PC / Escritorio)

    Entorno de Desarrollo: IntelliJ IDEA.

    Tecnologías: Java 11+, JavaFX, SQLite.

    Propósito: Gestión centralizada del padrón, diseño de plantillas dinámicas, auditoría de sesiones y exportación de reportes para la toma de decisiones.

Guía de Apertura para Desarrolladores

Para evitar conflictos entre las configuraciones de los entornos de desarrollo, siga estas instrucciones:

    Para trabajar en la App Móvil: Ejecute Android Studio y seleccione la opción "Abrir", apuntando directamente a la subcarpeta Modulo-Movil-Android.

    Para trabajar en el Sistema de PC: Ejecute IntelliJ IDEA y seleccione "Abrir", apuntando directamente a la subcarpeta Modulo-Escritorio-PC.
