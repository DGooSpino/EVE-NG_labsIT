# Lab 01: Enrutamiento Estático Multicapa en Arquitectura Jerárquica (Core y Distribución)

Este laboratorio simula una red empresarial simple de múltiples pisos utilizando una arquitectura de red jerárquica de dos capas (Núcleo/Core y Distribución). El objetivo principal es interconectar las dos redes locales (LAN) separadas físicamente (`Piso 1` y `Piso 2`) a través de un troncal redundante y rutas estáticas IPv4 configuradas en un entorno de simulación **EVE-NG**.

## Topología de Red
La topología implementa enlaces redundantes entre los routers del Core (`Core1`, `Core2`) y los routers de distribución (`Dist1`, `Dist2`) para asegurar la tolerancia a fallos en la capa de transporte.
[/lab-01makeLAN/01local.png]
---
## 🖧 Tabla de Direccionamiento IP

| Dispositivo | Interfaz | Dirección IP / Máscara | Descripción / Conexión |
| :--- | :--- | :--- | :--- |
| **Core1** | `e0/0` | `10.0.1.1/30` | Enlace troncal hacia Core2 |
| **Core1** | `e0/1` | `10.0.2.1/30` | Enlace hacia Dist1 (Piso 1) |
| **Core1** | `e0/2` | `10.0.4.1/30` | Enlace cruzado hacia Dist2 (Piso 2) |
| **Core2** | `e0/0` | `10.0.1.2/30` | Enlace troncal hacia Core1 |
| **Core2** | `e0/1` | `10.0.5.1/30` | Enlace hacia Dist2 (Piso 2) |
| **Core2** | `e0/2` | `10.0.3.1/30` | Enlace cruzado hacia Dist1 (Piso 1) |
| **Dist1** (Piso 1) | `e0/0` | `10.0.2.2/30` | Enlace hacia Core1 |
| **Dist1** (Piso 1) | `e0/1` | `10.0.5.2/30` | Enlace hacia Core2 |
| **Dist1** (Piso 1) | `e0/2` | `192.168.2.1/24` | Gateway LAN Piso 1 |
| **Dist2** (Piso 2) | `e0/0` | `10.0.4.2/30` | Enlace hacia Core1 |
| **Dist2** (Piso 2) | `e0/1` | `10.0.3.2/30` | Enlace hacia Core2 |
| **Dist2** (Piso 2) | `e0/2` | `192.168.1.1/24` | Gateway LAN Piso 2 |
