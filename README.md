# 🏗️ Sistema de Control Automatizado para Dosificación de Concreto

## Objetivo

Diseñar, implementar y validar un sistema de control automatizado (PLC + HMI) para la dosificación de concreto, que permita operar la planta de forma manual y automática mediante recetas configurables, con seguridad y repetibilidad.





## Integrantes y roles

|Integrante|Rol|
|-|-|
|**Juan José Lara Garcia**|Cableado de fuerza y control, lógica de arranque/paro de motores, manejo de alarmas y diseño/programación de pantallas HMI|
|**Néstor Luis De La Torre Cruz**|Montaje mecánico y etiquetado, arquitectura de software, configuración del PLC, recetas de dosificación y comunicación PLC–HMI|

Trabajo conjunto: selección de equipos, dimensionamiento del transformador, simulación, documentación y pruebas con carga real.



## Diagrama de bloques

```mermaid
flowchart LR
    OP(\[ Operador]) <--> HMI\[ HMI]
    HMI <-->|Comunicación| PLC\[ PLC]

    SEN\[ Sensores e instrumentos<br/>celdas de carga, límites] -->|Entradas| PLC
    PLC -->|Salidas| CTRL\[ Gabinete de control<br/>relevadores]
    CTRL --> POT\[ Gabinete de potencia<br/>contactores y guardamotores]
    POT --> MOT\[Motores y actuadores<br/>de la planta]

    ALIM\[Alimentación] --> TR\[Transformador de control]
    TR --> PLC
    TR --> CTRL
    ALIM --> POT
```

> Ajustar los bloques a la arquitectura final una vez seleccionados el PLC y la HMI.

